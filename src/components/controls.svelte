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
  height: 16px;
  margin-bottom: 28px;
  margin-left: -30px;
  cursor: pointer;
}

#controls label:hover {
  opacity: 1;
}

#controls label:before {
  position: absolute;
  display: block;
  width: 12px;
  height: 12px;
  margin-top: 3px;
  text-align: center;
  color: var(--text);
  z-index: 99;
}

#controls label span {
  display: block;
  margin-left: 36px;
  padding-top: 4px;
  font-size: 15px;
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
  margin-left: -35px;
  width: 15px;
  height: 15px;
  border: 1px solid var(--text);
  border-radius: 16px;
}

#controls input:checked[type="radio"]:after {
  content: "";
  display: block;
  top: 3px;
  margin-left: -39px;
  position: absolute;
  width: 13px;
  height: 13px;
  border-radius: 10px;
  background: var(--prime);
  z-index: 99;
  animation: simpleRot 10s linear infinite;
  transform-origin: 15px 5px;
}

#controls {
  padding-right: 32px;
  top: 12px;
}

@keyframes simpleRot {
  from {
    transform: rotate(0deg);
  }
  to {
    transform: rotate(359deg);
  }
}

.radio {
  box-shadow: inset 0 2px 2px 0 rgba(0, 0, 0, 0.3), inset 0 0 0 1px #d6d6d6,
    0 2px 0 0 white;
  background: #e5e4e4;
  padding: 20px 5px 5px;
  border-radius: 25px;
  background: linear-gradient(to bottom, #e5e4e4 1%, #f1f1f1 100%);
}
</style>

<script lang="ts">
export let threeD;
export let handle3D;
export let handleZoom;
export let zoom;
export let scale;
export let handleScale;

import Checkbox from "./UI/checkbox.svelte";
</script>

<div id="controls">
  <Checkbox
    handleCheckbox="{handle3D}"
    boolean="{threeD}"
    textOne="3D"
    textTwo="2D" />
  <Checkbox
    handleCheckbox="{handleZoom}"
    boolean="{zoom}"
    textOne="+"
    textTwo="-" />
  <div class="radio">
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
</div>
