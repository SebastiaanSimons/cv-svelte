<script lang="ts">
    import Title from "../style-components/Title.svelte";
    import SubTitle from "../style-components/SubTitle.svelte";
    import * as data from "../data.json";
</script>

<section>
    <Title title="Strengths" />

    {#each data["strengths"]["entries"] as strength}
        <div class="flex-container">
            <i class="{strength.icon} fa-lg icon" />
            <div>
                <SubTitle title={strength.title} />
                {@html strength.description}
            </div>
        </div>
    {/each}
</section>

<style>
    .flex-container {
        display: flex;
        align-items: center;
        font-size: 0.9em;
        gap: 20px;
        justify-content: space-between;
        margin-left: 5px;
        margin-bottom: 15px;
    }
    .icon {
        color: var(--main-color);
    }
</style>
