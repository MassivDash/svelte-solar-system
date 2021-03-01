<script lang="ts">
export let threeD;
export let handle3D;
export let handleZoom;
export let zoom;
export let scale;
export let handleScale;
</script>

<div id="controls">
  <label class="set-view">
    <input type="checkbox" bind:checked="{threeD}" on:change="{handle3D}" />
  </label>
  <label class="set-zoom">
    <input type="checkbox" bind:checked="{zoom}" on:change="{handleZoom}" />
  </label>
  <label>
    <input
      type="radio"
      class="set-speed"
      name="scale"
      on:change="{() => handleScale('speed')}"
      checked="{scale === 'speed'}" />
    <span>Speed</span>
  </label>
  <label>
    <input
      type="radio"
      class="set-size"
      name="scale"
      on:change="{handleScale('size')}"
      checked="{scale === 'size'}" />
    <span>Size</span>
  </label>
  <label>
    <input
      type="radio"
      class="set-distance"
      name="scale"
      on:change="{handleScale('distance')}"
      checked="{scale === 'distance'}" />
    <span>Distance</span>
  </label>
</div>
