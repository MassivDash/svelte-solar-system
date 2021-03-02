<script lang="ts">
import Navbar from "./components/navbar.svelte";
import Planets from "./components/planets.svelte";
import Controls from "./components/controls.svelte";
import Universe from "./components/universe.svelte";

import { onMount } from "svelte";
let showUi = false;
let zoom = false;
let threeD = false;
let controls = false;
let data = false;
let scale = "speed";
let choosenPlanet = "sun";

const planets = [
  "sun",
  "mercury",
  "venus",
  "earth",
  "mars",
  "jupiter",
  "saturn",
  "uranus",
  "neptune",
];

onMount(() => {
  const interval = setTimeout(() => {
    showUi = true;
    threeD = true;
  }, 200);

  return () => clearInterval(interval);
});

const handleData = () => (data = !data);
const handleControls = () => (controls = !controls);
const handleZoom = () => (zoom = !zoom);
const handle3D = () => (threeD = !threeD);
const handleScale = (value) => (scale = value);
const handlePlanet = (value) => (choosenPlanet = value);

$: bodyClass = `${!showUi ? "hide-UI" : "set-speed"} ${
  threeD ? "view-3D" : "view-2D opening "
} ${!zoom ? "zoom-large" : "zoom-close"} ${data ? "data-open" : "data-close"} ${
  controls ? "controls-open" : "controls-close"
}`;
</script>

<div class="{bodyClass}">
  <Navbar handleData="{handleData}" handleControls="{handleControls}" />
  <Planets
    choosenPlanet="{choosenPlanet}"
    handlePlanet="{handlePlanet}"
    planets="{planets}" />
  <Controls
    scale="{scale}"
    handleScale="{handleScale}"
    handleZoom="{handleZoom}"
    zoom="{zoom}"
    threeD="{threeD}"
    handle3D="{handle3D}" />
  <Universe
    choosenPlanet="{choosenPlanet}"
    scale="{scale}"
    planets="{planets}" />
</div>
