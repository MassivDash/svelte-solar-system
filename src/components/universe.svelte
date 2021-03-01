<script lang="ts">
export let scale: string;
export let choosenPlanet: string;

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
    <div id="solar-system" class={choosenPlanet}>
      <div id="mercury" class="orbit">
        <div class="pos">
          <div class="planet">
            <dl class="infos">
              <dt>Mercury</dt>
              <dd><span></span></dd>
            </dl>
          </div>
        </div>
      </div>
      <div id="venus" class="orbit">
        <div class="pos">
          <div class="planet">
            <dl class="infos">
              <dt>Venus</dt>
              <dd><span></span></dd>
            </dl>
          </div>
        </div>
      </div>
      <div id="earth" class="orbit">
        <div class="pos">
          <div class="orbit">
            <div class="pos">
              <div class="moon"></div>
            </div>
          </div>
          <div class="planet">
            <dl class="infos">
              <dt>Earth</dt>
              <dd><span></span></dd>
            </dl>
          </div>
        </div>
      </div>
      <div id="mars" class="orbit">
        <div class="pos">
          <div class="planet">
            <dl class="infos">
              <dt>Mars</dt>
              <dd><span></span></dd>
            </dl>
          </div>
        </div>
      </div>
      <div id="jupiter" class="orbit">
        <div class="pos">
          <div class="planet">
            <dl class="infos">
              <dt>Jupiter</dt>
              <dd><span></span></dd>
            </dl>
          </div>
        </div>
      </div>
      <div id="saturn" class="orbit">
        <div class="pos">
          <div class="planet">
            <div class="ring"></div>
            <dl class="infos">
              <dt>Saturn</dt>
              <dd><span></span></dd>
            </dl>
          </div>
        </div>
      </div>
      <div id="uranus" class="orbit">
        <div class="pos">
          <div class="planet">
            <dl class="infos">
              <dt>Uranus</dt>
              <dd><span></span></dd>
            </dl>
          </div>
        </div>
      </div>
      <div id="neptune" class="orbit">
        <div class="pos">
          <div class="planet">
            <dl class="infos">
              <dt>Neptune</dt>
              <dd><span></span></dd>
            </dl>
          </div>
        </div>
      </div>
      <div id="sun">
        <dl class="infos">
          <dt>Sun</dt>
          <dd><span></span></dd>
        </dl>
      </div>
    </div>
  </div>
</div>
