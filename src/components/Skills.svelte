<script lang="ts">
    import Title from "../style-components/Title.svelte";
    import SubTitle from "../style-components/SubTitle.svelte";
    import Level from "../sub-components/Level.svelte";
    import * as data from "../data.json";
</script>

<section>
    <Title title="Skills" />

    {#each data["skills"]["level_groups"] as skill_group}
        <SubTitle title={skill_group.group} />

        {#each skill_group.level_entries as skill}
            <div class="flex-container">
                <span class="skill-name"> {skill.name} </span>
                <Level level={skill.level} />
            </div>
        {/each}
    {/each}
</section>

<style>
    .flex-container {
        display: flex;
        justify-content: space-between;
        margin-bottom: 3px;
    }
    .skill-name {
        font-size: 0.9em;
    }
</style>
