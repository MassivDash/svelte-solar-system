<style>

h3 {
  font-size: 25px;
  margin: 15px 0;
  line-height: 1.7;
}

p {
  font-size: 18px;
  line-height: 1.7;
  margin-bottom: 10px;
}

.text-container {
  max-width: 1000px;
  margin: auto;
  transition: 0.6s ease-in;
}

.spacer {
  height: 100px;
}
</style>

<script lang="ts">

import IntersectionObserver from "./UI/intersectionObserver.svelte";

</script>
<IntersectionObserver let:intersecting top={-400}>
<div class="flex-holder">
  <div class={`text-container ${intersecting ? 'show' : 'hide'}`}>
    <h3>Birth of the Solar System</h3>
    <p>
      Our solar system began as part of a massive nebula cloud of molecular
      hydrogen and dust around 4.6 billion years ago. In a region of this dark
      cloud conditions allowed gravity to begin condensing the hydrogen until a
      substantial mass began to grow ever larger and hotter, eventually this
      mass collapsed in on itself, forming the early stage of a star called a
      protostar. The gravitational pull of the embryonic star caused a large
      disc of gas and dust to begin forming around it.
    </p>
    <p>
      Over millions of years pressure began to build up inside the protostar as
      it became hotter and denser until eventually nuclear fusion began in its
      core, giving birth to the sun as we know it. During this time the disc of
      gas and dust that had formed around the star had also began condensing
      into ever growing orbiting bodies. In time they would go on to form the
      planets, moons and other objects in our solar system.
    </p>
    <div class="spacer"></div>
  </div>
</div>
</IntersectionObserver>