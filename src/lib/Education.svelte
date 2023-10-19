<script lang="ts">
	import Panel from "./Panel.svelte";
	import List from "./List.svelte";

	const educationData = [
		"High School Diploma",
		"Completed Military Service",
	];
</script>

<Panel bgEnabled>
	<h3 class="text-xl font-bold">Education:</h3>

	<List data={educationData} let:item>
		<span>{item}</span>
	</List>
</Panel>
