<script lang="ts">
    export let bullet_points: {
        text: string;
    }[];
    export let font_size = "0.9em";
</script>

<ul>
    {#each bullet_points as bullet}
        <li style:font-size={font_size}>
            {bullet.text}
        </li>
    {/each}
</ul>

<style>
    ul {
        padding-left: 20px;
        margin: 10px 0px;
    }
    li {
        margin-bottom: 5px;
    }
</style>
