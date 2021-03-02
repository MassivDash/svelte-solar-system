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

import Checkbox from './UI/checkbox.svelte';
</script>

<div id="controls">
    <Checkbox handleCheckbox={handle3D} boolean={threeD} textOne="3D" textTwo="2D" />
    <Checkbox handleCheckbox={handleZoom} boolean={zoom} textOne="+" textTwo="-" />
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
