<script lang="ts">
	import Panel from "./Panel.svelte";
	import List from "./List.svelte";

	const additionalInfoData = [
		{ title: "Languages", text: "BY, EN, RU. Basic proficiency in Polish." },
		{
			title: "Interests",
			text: "Passionate about video gaming, city explorations, and cherishing moments with my child.",
		},
	];
</script>

<Panel>
	<h3 class="text-xl font-bold">Additional Info</h3>
	<List data={additionalInfoData} let:item>
		<h4 class="text font-semibold">{item.title}:</h4>
		<span>{item.text}</span>
	</List>
</Panel>
