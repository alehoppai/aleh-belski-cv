<script lang="ts">
	export let bgEnabled = false;
</script>

<section
	class="flex flex-col gap-4 p-4"
	class:bg-slate-200={bgEnabled}
	class:dark:bg-slate-800={bgEnabled}
>
	<slot />
</section>
