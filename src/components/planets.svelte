<script lang="ts">
    export let choosenPlanet: string;
    export let handlePlanet;
    export let planets;

</script>

<div id="data">
    {#each planets as planet, i}
        <a class={`${planet} ${choosenPlanet === planet ? 'active' : ''}`} title={planet} on:click={() => handlePlanet(planet)} href={`#${planet}speed`}>{planet}</a>
    {/each}
</div>
