<script lang="ts">
	import { Icon, Phone, Envelope, Link, MapPin, Clipboard } from "svelte-hero-icons";
	import Panel from "./Panel.svelte";

	const tel = "+48572881022";
	const email = "aleh_belski@outlook.com";
	const location = "Warsaw, Poland";
	const linkedInUri = "https://www.linkedin.com/in/aleh-belski-fullstack-js/";

	const contactsData = [
		{
			icon: Phone,
			text: tel,
			link: `tel:${tel}`,
		},
		{
			icon: Envelope,
			text: email,
			link: `mailto:${email}`,
		},
		{
			icon: MapPin,
			text: location,
			link: `https://www.google.com/maps/place/${location}`,
		},
		{
			icon: Link,
			text: "Me on LinkedIn",
			link: linkedInUri,
		},
	];

	const copyToClipboard = () => {
		navigator.clipboard.writeText("Tel: " + tel + "\nEmail: " + email + "\nLocation: " + location + "\nLinkedIn: " + linkedInUri);
	};
</script>

<Panel bgEnabled>
	<div class="flex flex-row items-center justify-between">
		<h3 class="text-xl font-bold">CONTACTS</h3>
		<button
			class="w-10 h-10 p-2 transition-colors hover:bg-slate-300 no-print"
			on:click={copyToClipboard}
			title="Copy contacts"
		>
			<Icon src={Clipboard} />
		</button>
	</div>

	<ul>
		{#each contactsData as contact}
			<li class="my-4">
				<a
					class="flex flex-row gap-2"
					href={contact.link}
					target="_blank"
					rel="noopener noreferrer"
				>
					<Icon class="w-6 h-6" src={contact.icon} />
					<span>{contact.text}</span>
				</a>
			</li>
		{/each}
	</ul>
</Panel>
