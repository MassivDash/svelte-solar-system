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
