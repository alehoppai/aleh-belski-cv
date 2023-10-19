<script lang="ts">
	import Panel from "./Panel.svelte";
	import List from "./List.svelte";

	const techSkillsData = [
		{ title: "Frontend", skills: ["Svelte-kit", "Tailwindcss", "React/Next", "Sass"] },
		{ title: "Backend", skills: ["Express.js", "Nest.js"] },
		{ title: "Databases", skills: ["MySQL", "MongoDB, PostgreSQL"] },
		{ title: "Mobile", skills: ["React-native", "SwiftUI"] },
		{ title: "DevOps/Tools", skills: ["Docker", "AWS", "Git", "Firebase"] },
	];
</script>

<Panel>
	<h3 class="text-xl font-bold">Technical Skills:</h3>
	<List data={techSkillsData} let:item>
		<h4 class="text font-semibold">{item.title}:</h4>

		{#each item.skills as skill, i}
			<span>{skill}{i !== item.skills.length - 1 ? "," : ""}&nbsp;</span>
		{/each}
	</List>
</Panel>
