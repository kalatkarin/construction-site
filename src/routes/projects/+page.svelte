<script lang="ts">
    import Categories from './Categories.svelte';
    const { data } = $props();
</script>

<div class="place-items-center">
    <div class=" m-[100px] grid grid-cols-5 place-items-center items-stretch gap-11">
        {#each data.summaries as cat}
            <Categories cat={cat.cat} icon={cat.icon} link={cat.link}></Categories>
        {/each}
    </div>
</div>
