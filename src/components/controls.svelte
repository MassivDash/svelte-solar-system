<style>
#controls label {
  color: var(--text);
  display: block;
  position: relative;
  text-decoration: none;
}

#controls label:hover {
  color: var(--second);
}

#controls {
  z-index: 99;
  position: absolute;
  opacity: 1;
  top: 49px;
  padding: 16px;
}

#controls label {
  opacity: 0.6;
  height: 24px;
  margin-bottom: 28px;
}

#controls label:hover {
  opacity: 1;
}

#controls label:before {
  position: absolute;
  display: block;
  width: 20px;
  height: 20px;
  margin-top: 3px;
  text-align: center;
  color: var(--text);
  z-index: 99;
}

#controls label span {
  display: block;
  margin-left: 36px;
  padding-top: 4px;
  font-size: 18px;
  color: var(--text);
}

#controls input {
  display: block;
  appearance: none;
}

#controls input[type="radio"]:before {
  content: "";
  display: block;
  position: absolute;
  width: 22px;
  height: 22px;
  border: 2px solid var(--text);
  border-radius: 16px;
}

#controls input:checked[type="radio"]:after {
  content: "";
  display: block;
  top: 3px;
  margin-left: 3px;
  position: absolute;
  width: 20px;
  height: 20px;
  border-radius: 10px;
  background: var(--text);
  z-index: 99;
}

#controls input[type="checkbox"]:before {
  content: "";
  display: block;
  position: absolute;
  width: 100px;
  height: 22px;
  border: 2px solid var(--text);
  border-radius: 16px;
}

#controls input[type="checkbox"]:after {
  content: "";
  display: block;
  top: 3px;
  position: absolute;
  width: 20px;
  height: 20px;
  border-radius: 10px;
  background: var(--text);
  z-index: 99;
}

#controls label.set-view:before {
  font: bold small-caps 11px/20px sans-serif;
}

#controls label.set-zoom:before {
  font: normal small-caps 18px/14px sans-serif;
}

#controls {
  padding-right: 32px;
  top: 12px;
}
</style>

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
    <span>speed</span>
  </label>
  <label>
    <input
      type="radio"
      class="set-size"
      name="scale"
      on:change="{handleScale('size')}"
      checked="{scale === 'size'}" />
    <span>size</span>
  </label>
  <label>
    <input
      type="radio"
      class="set-distance"
      name="scale"
      on:change="{handleScale('distance')}"
      checked="{scale === 'distance'}" />
    <span>distance</span>
  </label>
</div>
