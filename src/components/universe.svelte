<script lang="ts">
export let scale: string;
export let choosenPlanet: string;
export let planets: string[];
export let handlePlanet;

const scaleClass = (scale) => {
  if (scale === "speed") {
    return "scale-stretched set-speed";
  }

  if (scale === "size") {
    return "scale-s set-size";
  }

  if (scale === "distance") {
    return "scale-d set-distance";
  }

  return "scale-stretched";
};

$: universeClass = scaleClass(scale);
</script>

<div id="universe" class="{universeClass}">
  <div id="galaxy">
    <div id="solar-system" class="{choosenPlanet}">
      {#each planets as planet, i}
        {#if planet !== "sun"}
          <div id="{planet}" class="orbit" >
            <div class="pos" on:click="{() => handlePlanet(planet)}" title={planet}>
              <div
                class="{`planet ${
                  choosenPlanet === planet ? '' : 'grey-filter'
                }`}">
                {#if planet === "saturn"}
                  <div class="ring"></div>
                {/if}
                <dl class="infos">
                  <dt>{planet}</dt>
                  <dd><span></span></dd>
                </dl>
              </div>
            </div>
          </div>
        {/if}
        {#if planet === "sun"}
          <div
            id="{planet}"
            class="{`${choosenPlanet === planet ? '' : 'grey-filter'}`}">
            <dl class="infos">
              <dt>{planet}</dt>
              <dd><span></span></dd>
            </dl>
          </div>
        {/if}
      {/each}
    </div>
  </div>
</div>
