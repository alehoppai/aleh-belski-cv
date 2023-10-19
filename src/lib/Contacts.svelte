<script lang="ts">
	import { Icon, Phone, Envelope, Link, MapPin, Clipboard } from "svelte-hero-icons";
	import Panel from "./Panel.svelte";
	import List from "./List.svelte";

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
		navigator.clipboard.writeText("**PRIORITY CONTACT**\nALEH BELSKI, Fullstack Software Developer\nTel: " + tel + "\nEmail: " + email + "\nLocation: " + location + "\nLinkedIn: " + linkedInUri);
	};
</script>

<Panel bgEnabled>
	<div class="flex flex-row items-center justify-between">
		<h3 class="text-xl font-bold">CONTACTS</h3>
		<button
			class="w-10 h-10 p-2 transition-colors hover:bg-slate-300 dark:hover:bg-slate-700 no-print"
			on:click={copyToClipboard}
			title="Copy contacts"
		>
			<Icon src={Clipboard} />
		</button>
	</div>

	<List data={contactsData} let:item>
		<a
			class="flex flex-row gap-2"
			href={item.link}
			target="_blank"
			rel="noopener noreferrer"
		>
			<Icon class="w-6 h-6" src={item.icon} />
			<span>{item.text}</span>
		</a>
	</List>
</Panel>
