<style>
.title-holder {
  display: flex;
  justify-content: flex-start;
  align-items: center;
  position: absolute;
  top: 10px;
  left: 10px;
}

.logo-holder {
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: center;
}

.text-holder {
  margin-left: 35px;
  text-align: left;
}

img {
  max-width: 45px;
}

h1 {
  font-size: 80px;
  color: var(--spaceoutBlue);
  line-height: 1;
  font-weight: 300;
  font-family: "Paytone one";
  margin-top: -40px;
  text-shadow: 1px 1px 2px black;
}

span {
  color: var(--prime);
}

h2 {
  margin-left: 20px;
  font-size: 20px;
  color: var(--black);
}
</style>

<script lang="ts">
let logo = "../../img/City.png";
</script>

<div class="title-holder">
  <div class="logo-holder">
    <img src="{logo}" alt="spaceout.pl" />
    <div class="text-holder">
      <h1>s</h1>
    </div>
  </div>
  <h2><span>svelte</span> solar system</h2>
</div>
