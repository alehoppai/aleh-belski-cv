<script lang="ts">
	import { Icon, Printer } from "svelte-hero-icons";

	const getPrintPdf = () => {
		window.print();
	};
</script>

<header class="flex flex-row justify-between items-center">
	<div>
		<h3 class="text-xl font-semibold">Fullstack Software Developer</h3>
		<h1 class="text-3xl font-bold">Aleh Belski</h1>
	</div>

	<button
		class="w-10 h-10 p-2 transition-colors hover:bg-slate-300 no-print"
		on:click={getPrintPdf}
		title="Print"
	>
		<Icon src={Printer} />
	</button>
</header>
