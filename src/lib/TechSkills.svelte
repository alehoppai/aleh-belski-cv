<script lang="ts">
    import Panel from "./Panel.svelte";

    const techSkillsData = [
        { title: "Frontend", skills: ["Svelte-kit", "Tailwindcss", "React/Next", "Sass"] },
        { title: "Backend", skills: ["Express.js", "Nest.js"] },
        { title: "Databases", skills: ["MySQL", "MongoDB, PostgreSQL"] },
        { title: "Mobile", skills: ["React-native", "SwiftUI"] },
        { title: "DevOps/Tools", skills: ["Docker", "AWS", "Git", "Firebase"] }
    ]
</script>

<Panel>
    <h3 class="text-xl font-bold">Technical Skills:</h3>
    <ul>
        {#each techSkillsData as skill}
            <li class="my-4">
                <strong>{skill.title}:</strong>

                {#each skill.skills as s, i}
                    <span>{s}{i !== skill.skills.length - 1 && ","}&nbsp;</span>
                {/each}
            </li>
        {/each}
    </ul>
</Panel>