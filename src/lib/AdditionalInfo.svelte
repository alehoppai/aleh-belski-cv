<script lang="ts">
    import Panel from "./Panel.svelte";


    const additionalInfoData = [
        { title: "Languages", text: "BY, EN, RU. Basic proficiency in Polish." },
        { title: "Interests", text: "Passionate about video gaming, city explorations, and cherishing moments with my child." },
    ]
</script>

<Panel>
    <h3 class="text-xl font-bold">Additional Info</h3>
    <ul>
        {#each additionalInfoData as info}
            <li class="my-4">
                <strong>{info.title}:</strong>
                <span>{info.text}</span>
            </li>
        {/each}
    </ul>
</Panel>

