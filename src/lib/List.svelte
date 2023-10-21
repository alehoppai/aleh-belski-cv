<script lang="ts">
	export let data: any[];
</script>

<ul>
	{#each data as item}
		<li class="my-4">
			<slot {item} />
		</li>
	{/each}
</ul>
