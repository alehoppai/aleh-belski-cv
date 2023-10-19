<script lang="ts">
	import "./app.css";

	import Contacts from "./lib/Contacts.svelte";
	import TechSkills from "./lib/TechSkills.svelte";
	import Summary from "./lib/Summary.svelte";
	import Header from "./lib/Header.svelte";
	import Education from "./lib/Education.svelte";
	import AdditionalInfo from "./lib/AdditionalInfo.svelte";
	import ProfessionalExperience from "./lib/ProfessionalExperience.svelte";
</script>

<div
	class="bg-slate-50 dark:bg-slate-950 text-slate-950 dark:text-slate-50 w-full flex flex-col items-center"
>
	<div class="flex flex-col p-12 max-w-[1200px]">
		<Header />

		<div class="my-12 h-1px border border-slate-200 dark:border-slate-800"></div>

		<div class="flex flex-row gap-12 w-full">
			<div class="flex flex-col gap-6 w-1/3">
				<Contacts />
				<TechSkills />
				<Education />
				<AdditionalInfo />
			</div>
			<div class="flex flex-col w-2/3">
				<Summary />
				<div class="my-6 h-1px border border-slate-200 dark:border-slate-800"></div>
				<ProfessionalExperience />
			</div>
		</div>
	</div>
</div>
