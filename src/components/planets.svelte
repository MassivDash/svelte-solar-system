<style>
#data a {
  color: var(--text);
  display: block;
  position: relative;
  text-decoration: none;
  margin-bottom: 1px;
  padding: 6px 10px;
  font-size: 18px;
}

#data a:hover {
  color: var(--second);
}

#data a.active {
  color: var(--prime);
}

#data {
  z-index: 99;
  position: absolute;
  opacity: 1;
  bottom: 30px;
  padding: 16px;
  transition: 0.7s ease-in-out;
}

@media screen and (min-width: 1000px) {
  #data {
    background: transparent;
  }

  #data {
    position: absolute;
    top: inherit;
    bottom: 25px;
    width: 100%;
    text-align: center;
  }

  #data a {
    display: inline-block;
    text-align: center;
    font-size: 20px;
    padding: 15px 15px;
  }
}
</style>

<script lang="ts">
export let choosenPlanet: string;
export let handlePlanet;
export let planets: string[];
</script>

<div id="data">
  {#each planets as planet, i}
    <a
      class="{`${planet} ${choosenPlanet === planet ? 'active' : ''}`}"
      title="{planet}"
      on:click="{() => handlePlanet(planet)}"
      href="{`#${planet}speed`}">{planet}</a>
  {/each}
</div>
