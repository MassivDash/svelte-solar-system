<style>
#navbar {
  z-index: 99;
  position: absolute;
  top: 0;
  left: 0;
  padding: 16px;
  width: 100%;
  height: 48px;
}

#navbar a {
  color: var(--text);
  display: block;
  position: relative;
  text-decoration: none;
}

#navbar a:hover {
  color: var(--second);
}

#navbar a {
  position: absolute;
  top: 0;
  height: 48px;
  padding: 16px;
  font-size: 14px;
}

@media screen and (min-width: 1000px) {
  #navbar a {
    display: none;
  }
}
</style>

<script lang="ts">
export let handleData: (value) => void;
export let handleControls: (value) => void;
</script>

<div id="navbar">
  <a id="toggle-data" href="#data" on:click="{handleData}"
    ><i class="icon-data"></i>Data</a>
  <a id="toggle-controls" href="#controls" on:click="{handleControls}"
    ><i class="icon-controls"></i>Controls</a>
</div>
