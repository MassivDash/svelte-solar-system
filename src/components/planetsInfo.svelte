<style>
:root {
  --mercury-image: url(../../img/mercury2.jpg);
  --mercury-tilt: rotate(0.034deg);
  --mercury-day: 1407.6;
  --mercury-color: #999999;
  --venus-image: url(../../img/venus2.jpg);
  --venus-tilt: rotate(177.3deg);
  --venus-day: 5832.5;
  --venus-color: #e8cda2;
  --earth-image: url(../../img/earth.jpg);
  --earth-tilt: rotate(23.26deg);
  --earth-day: 23.9;
  --earth-color: #b3caff;
  --mars-image: url(../../img/mars.jpg);
  --mars-tilt: rotate(25.2deg);
  --mars-day: 24.6;
  --mars-color: #c07158;
  --jupiter-image: url(../../img/jupiter.jpg);
  --jupiter-tilt: rotate(3.1deg);
  --jupiter-day: 9.9;
  --jupiter-color: #c9b5a4;
  --saturn-image: url(../../img/saturn.jpg);
  --saturn-tilt: rotate(26.7deg);
  --saturn-day: 10.7;
  --saturn-color: #f0e2c4;
  --uranus-image: url(../../img/uranus2.jpg);
  --uranus-tilt: rotate(97.8deg);
  --uranus-day: 17.2;
  --uranus-color: #b8d8e1;
  --neptune-image: url(../../img/neptune.jpg);
  --neptune-tilt: rotate(28.3deg);
  --neptune-day: 16.1;
  --neptune-color: #5e73bb;
  --pluto-image: url(../../img/pluto.jpg);
  --pluto-tilt: rotate(122.5deg);
  --pluto-day: 153.3;
  --pluto-color: #c3b6aa;
  --sun-image: url(../../img/sun.jpg);
  --sun-tilt: rotate(0deg);
  --sun-day: 600;
  --sun-color: #ffd07957;
}

.planetsInfo-holder {
  margin: auto;
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: auto;
  grid-gap: 100px;
  max-width: 1000px;
  align-items: flex-start;
  justify-items: flex-start;
  justify-content: flex-start;
  padding-bottom: 100px;
}

@keyframes planetRotate {
  0% {
    background-position: 0% center;
  }
  100% {
    background-position: -200% center;
  }
}

.card {
  display: flex;
  flex-direction: column;
  align-items: center;
  position: relative;
  transition: 1.2s ease-in;
}
.card--mercury .planet__atmosphere {
  box-shadow: inset 10px 0px 12px -2px rgba(255, 255, 255, 0.2),
    inset -70px 0px 50px 0px black, -5px 0px 10px -4px var(--mercury-color);
}
.card--mercury .planet__surface {
  background-image: var(--mercury-image);
  transform: var(--mercury-tilt) scale(1.2);
  animation: planetRotate calc(var(--mercury-day) * 0.1s) linear infinite;
}
.card--mercury .card__planet::before {
  transform: var(--mercury-tilt) scale(1.2);
  border-color: var(--mercury-color);
  color: var(--mercury-color);
}
.card--mercury .tilt__icon {
  transform: var(--mercury-tilt);
  color: var(--mercury-color);
}
.card--venus .planet__atmosphere {
  box-shadow: inset 10px 0px 12px -2px rgba(255, 255, 255, 0.2),
    inset -70px 0px 50px 0px black, -5px 0px 10px -4px var(--venus-color);
}
.card--venus .planet__surface {
  background-image: var(--venus-image);
  transform: var(--venus-tilt) scale(1.2);
  animation: planetRotate calc(var(--venus-day) * 0.1s) linear infinite;
}
.card--venus .card__planet::before {
  transform: var(--venus-tilt) scale(1.2);
  border-color: var(--venus-color);
  color: var(--venus-color);
}
.card--venus .tilt__icon {
  transform: var(--venus-tilt);
  color: var(--venus-color);
}
.card--earth .planet__atmosphere {
  box-shadow: inset 10px 0px 12px -2px rgba(255, 255, 255, 0.2),
    inset -70px 0px 50px 0px black, -5px 0px 10px -4px var(--earth-color);
}
.card--earth .planet__surface {
  background-image: var(--earth-image);
  transform: var(--earth-tilt) scale(1.2);
  animation: planetRotate calc(var(--earth-day) * 0.1s) linear infinite;
}
.card--earth .card__planet::before {
  transform: var(--earth-tilt) scale(1.2);
  border-color: var(--earth-color);
  color: var(--earth-color);
}
.card--earth .tilt__icon {
  transform: var(--earth-tilt);
  color: var(--earth-color);
}
.card--mars .planet__atmosphere {
  box-shadow: inset 10px 0px 12px -2px rgba(255, 255, 255, 0.2),
    inset -70px 0px 50px 0px black, -5px 0px 10px -4px var(--mars-color);
}
.card--mars .planet__surface {
  background-image: var(--mars-image);
  transform: var(--mars-tilt) scale(1.2);
  animation: planetRotate calc(var(--mars-day) * 0.1s) linear infinite;
}
.card--mars .card__planet::before {
  transform: var(--mars-tilt) scale(1.2);
  border-color: var(--mars-color);
  color: var(--mars-color);
}
.card--mars .tilt__icon {
  transform: var(--mars-tilt);
  color: var(--mars-color);
}
.card--jupiter .planet__atmosphere {
  box-shadow: inset 10px 0px 12px -2px rgba(255, 255, 255, 0.2),
    inset -70px 0px 50px 0px black, -5px 0px 10px -4px var(--jupiter-color);
}
.card--jupiter .planet__surface {
  background-image: var(--jupiter-image);
  transform: var(--jupiter-tilt) scale(1.2);
  animation: planetRotate calc(var(--jupiter-day) * 0.1s) linear infinite;
}
.card--jupiter .card__planet::before {
  transform: var(--jupiter-tilt) scale(1.2);
  border-color: var(--jupiter-color);
  color: var(--jupiter-color);
}
.card--jupiter .tilt__icon {
  transform: var(--jupiter-tilt);
  color: var(--jupiter-color);
}
.card--saturn .planet__atmosphere {
  box-shadow: inset 10px 0px 12px -2px rgba(255, 255, 255, 0.2),
    inset -70px 0px 50px 0px black, -5px 0px 10px -4px var(--saturn-color);
}
.card--saturn .planet__surface {
  background-image: var(--saturn-image);
  transform: var(--saturn-tilt) scale(1.2);
  animation: planetRotate calc(var(--saturn-day) * 0.1s) linear infinite;
}
.card--saturn .card__planet::before {
  transform: var(--saturn-tilt) scale(1.2);
  border-color: var(--saturn-color);
  color: var(--saturn-color);
}
.card--saturn .tilt__icon {
  transform: var(--saturn-tilt);
  color: var(--saturn-color);
}
.card--uranus .planet__atmosphere {
  box-shadow: inset 10px 0px 12px -2px rgba(255, 255, 255, 0.2),
    inset -70px 0px 50px 0px black, -5px 0px 10px -4px var(--uranus-color);
}
.card--uranus .planet__surface {
  background-image: var(--uranus-image);
  transform: var(--uranus-tilt) scale(1.2);
  animation: planetRotate calc(var(--uranus-day) * 0.1s) linear infinite;
}
.card--uranus .card__planet::before {
  transform: var(--uranus-tilt) scale(1.2);
  border-color: var(--uranus-color);
  color: var(--uranus-color);
}
.card--uranus .tilt__icon {
  transform: var(--uranus-tilt);
  color: var(--uranus-color);
}
.card--neptune .planet__atmosphere {
  box-shadow: inset 10px 0px 12px -2px rgba(255, 255, 255, 0.2),
    inset -70px 0px 50px 0px black, -5px 0px 10px -4px var(--neptune-color);
}
.card--neptune .planet__surface {
  background-image: var(--neptune-image);
  transform: var(--neptune-tilt) scale(1.2);
  animation: planetRotate calc(var(--neptune-day) * 0.1s) linear infinite;
}
.card--neptune .card__planet::before {
  transform: var(--neptune-tilt) scale(1.2);
  border-color: var(--neptune-color);
  color: var(--neptune-color);
}
.card--neptune .tilt__icon {
  transform: var(--neptune-tilt);
  color: var(--neptune-color);
}
.card--pluto .planet__atmosphere {
  box-shadow: inset 10px 0px 12px -2px rgba(255, 255, 255, 0.2),
    inset -70px 0px 50px 0px black, -5px 0px 10px -4px var(--pluto-color);
}
.card--pluto .planet__surface {
  background-image: var(--pluto-image);
  transform: var(--pluto-tilt) scale(1.2);
  animation: planetRotate calc(var(--pluto-day) * 0.1s) linear infinite;
}
.card--pluto .card__planet::before {
  transform: var(--pluto-tilt) scale(1.2);
  border-color: var(--pluto-color);
  color: var(--pluto-color);
}
.card--pluto .tilt__icon {
  transform: var(--pluto-tilt);
  color: var(--pluto-color);
}
.card--sun .planet__atmosphere {
  box-shadow: inset 10px 0px 12px -2px rgba(255, 255, 255, 0.2),
    inset -70px 0px 50px 0px black, -5px 0px 10px -4px var(--sun-color);
}
.card--sun .planet__surface {
  background-image: var(--sun-image);
  transform: var(--sun-tilt) scale(1.2);
  animation: planetRotate calc(var(--sun-day) * 0.1s) linear infinite;
}
.card--sun .card__planet::before {
  transform: var(--sun-tilt) scale(1.2);
  border-color: var(--sun-color);
  color: var(--sun-color);
}
.card--sun .tilt__icon {
  transform: var(--sun-tilt);
  color: var(--sun-color);
}

.card__planet::before {
  content: "";
  position: absolute;
  height: 190px;
  z-index: -2;
  left: 50%;
  top: 0%;
  border-left: 1px dashed rgba(255, 255, 255, 0.25);
}

.planet__atmosphere {
  height: 190px;
  width: 190px;
  position: relative;
  background: radial-gradient(
    circle at 30% 50%,
    rgba(255, 255, 255, 0.3) 0%,
    rgba(255, 255, 255, 0) 65%
  );
  border-radius: 100px;
  overflow: hidden;
}
.planet__surface {
  position: absolute;
  height: 100%;
  width: 100%;
  z-index: -1;
  background-size: cover;
}

.card--sun .planet__atmosphere {
  box-shadow: 0px 0px 10px 0px var(--sun-color),
    0px 0px 1000px -2px var(--sun-color);
}

.card__info {
  width: 100%;
}

.info__title {
  text-align: center;
  font-size: 28px;
  margin: 30px;
}
.info__form {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}
.info__item {
  display: flex;
  align-items: flex-end;
  margin-bottom: 5px;
  font-size: 14px;
  padding: 0 20px;
  transition: 0.8s ease-in;
  transition-delay: 0.3s; 
}
.info__item .tilt__icon {
  margin: 0 5px;
}
.info__label {
  font-size: 11px;
  color: var(--prime)
}
.info__line {
  flex: 1;
  margin: 0 5px;
  border-bottom: 1px dashed rgba(255, 255, 255, 0.3);
}

p {
  font-size: 16px;
  line-height: 1.7;
  margin-top: 30px;
  margin-bottom: 10px;
  margin-left: 60px;
}

.article-holder {
    display: flex;
    width: 100%;
    height: 100%;
    padding: 20px 0;
    justify-content: center;
    margin: 100px auto;
}

.show {
    opacity: 1
}

.hide {
    opacity: 0
}

</style>

<script lang="ts">
import IntersectionObserver from "./UI/intersectionObserver.svelte";

let planetsInfo = [
  { name: "sun", tilt: "0", day: "~600", year: "0", text: "The Sun is the star at the center of the Solar System. It is a nearly perfect sphere of hot plasma, heated to incandescence by nuclear fusion reactions in its core, radiating the energy mainly as visible light and infrared radiation. It is by far the most important source of energy for life on Earth. Its diameter is about 1.39 million kilometres (864,000 miles), or 109 times that of Earth. Its mass is about 330,000 times that of Earth, and accounts for about 99.86% of the total mass of the Solar System. Roughly three quarters of the Sun's mass consists of hydrogen (~73%); the rest is mostly helium (~25%), with much smaller quantities of heavier elements, including oxygen, carbon, neon, and iron." },
  { name: "mercury", tilt: "0.034", day: "1,407", year: "88", text: "Mercury is the smallest and closest planet to the sun in the Solar System. Its orbit around the Sun takes 87.97 Earth days, the shortest of all the planets in the Solar System. It is named after the Greek god Hermes (Ερμής), translated into Latin as Mercurius (Mercury), god of commerce, messenger of the gods, mediator between gods and mortals." },
  { name: "venus", tilt: "177.3", day: "5,832", year: "224.7", text: "Venus is the second planet from the Sun. It is named after the Roman goddess of love and beauty. As the brightest natural object in Earth's night sky after the Moon, Venus can cast shadows and can be, on rare occasion, visible to the naked eye in broad daylight. Venus lies within Earth's orbit, and so never appears to venture far from the Sun, either setting in the west just after dusk or rising in the east a little while before dawn. Venus orbits the Sun every 224.7 Earth days. With a rotation period of 243 Earth days, it takes longer to rotate about its axis than any other planet in the Solar System by far, and does so in the opposite direction to all but Uranus (meaning the Sun rises in the west and sets in the east). Venus does not have any moons, a distinction it shares only with Mercury among the planets in the Solar System." },
  { name: "earth", tilt: "23.26", day: "23.9", year: "365.2", text: "Earth is the third planet from the Sun and the only astronomical object known to harbor life. About 29% of Earth's surface is land consisting of continents and islands. The remaining 71% is covered with water, mostly by oceans but also by lakes, rivers, and other fresh water, which together constitute the hydrosphere. Much of Earth's polar regions are covered in ice. Earth's outer layer is divided into several rigid tectonic plates that migrate across the surface over many millions of years. Earth's interior remains active with a solid iron inner core, a liquid outer core that generates Earth's magnetic field, and a convecting mantle that drives plate tectonics." },
  { name: "mars", tilt: "25.2", day: "24.6", year: "687", text: "Mars is the fourth planet from the Sun and the second-smallest planet in the Solar System, being larger than only Mercury. In English, Mars carries the name of the Roman god of war and is often referred to as the \"Red Planet\". The latter refers to the effect of the iron oxide prevalent on Mars's surface, which gives it a reddish appearance distinctive among the astronomical bodies visible to the naked eye. Mars is a terrestrial planet with a thin atmosphere, with surface features reminiscent of the impact craters of the Moon and the valleys, deserts and polar ice caps of Earth." },
  { name: "jupiter", tilt: "3.1", day: "9.9", year: "4,331", text: "Jupiter is the fifth planet from the Sun and the largest in the Solar System. It is a gas giant with a mass one-thousandth that of the Sun, but two and a half times that of all the other planets in the Solar System combined. Jupiter is the third-brightest natural object in the Earth's night sky after the Moon and Venus. It has been observed since pre-historic times and is named after the Roman god Jupiter." },
  { name: "saturn", tilt: "26.7", day: "10.7", year: "10,747", text: "Saturn is the sixth planet from the Sun and the second-largest in the Solar System, after Jupiter. It is a gas giant with an average radius of about nine times that of Earth. It only has one-eighth the average density of Earth; however, with its larger volume, Saturn is over 95 times more massive. Saturn is named after the Roman god of wealth and agriculture; its astronomical symbol (♄) represents the god's sickle. The Romans named the seventh day of the week Saturday, Sāturni diēs (\"Saturn's Day\") no later than the 2nd century for the planet Saturn." },
  { name: "uranus", tilt: "97.8", day: "17.2", year: "30,589", text: "Uranus is the seventh planet from the Sun. Its name is a reference to the Greek god of the sky, Uranus, who, according to Greek mythology, was the grandfather of Zeus (Jupiter) and father of Cronus (Saturn). It has the third-largest planetary radius and fourth-largest planetary mass in the Solar System. Uranus is similar in composition to Neptune, and both have bulk chemical compositions which differ from that of the larger gas giants Jupiter and Saturn. For this reason, scientists often classify Uranus and Neptune as \"ice giants\" to distinguish them from the other gas giants. Uranus's atmosphere is similar to Jupiter's and Saturn's in its primary composition of hydrogen and helium, but it contains more \"ices\" such as water, ammonia, and methane, along with traces of other hydrocarbons. It has the coldest planetary atmosphere in the Solar System, with a minimum temperature of 49 K (−224 °C; −371 °F), and has a complex, layered cloud structure with water thought to make up the lowest clouds and methane the uppermost layer of clouds.The interior of Uranus is mainly composed of ices and rock." },
  { name: "neptune", tilt: "28.3", day: "16.1", year: "59,800", text: "Neptune is the eighth and farthest-known Solar planet from the Sun. In the Solar System, it is the fourth-largest planet by diameter, the third-most-massive planet, and the densest giant planet. It is 17 times the mass of Earth, slightly more massive than its near-twin Uranus. Neptune is denser and physically smaller than Uranus because its greater mass causes more gravitational compression of its atmosphere. The planet orbits the Sun once every 164.8 years at an average distance of 30.1 AU (4.5 billion km; 2.8 billion mi). It is named after the Roman god of the sea and has the astronomical symbol ♆, a stylised version of the god Neptune's trident." },
  { name: "pluto", tilt: "122.5", day: "153.3", year: "90,560", text: "Pluto (minor planet designation: 134340 Pluto) is a dwarf planet in the Kuiper belt, a ring of bodies beyond the orbit of Neptune. It was the first and the largest Kuiper belt object to be discovered. After Pluto was discovered in 1930, it was declared to be the ninth planet from the Sun. Beginning in the 1990s, its status as a planet was questioned following the discovery of several objects of similar size in the Kuiper belt, including the dwarf planet Eris. This led the International Astronomical Union (IAU) in 2006 to formally define the term \"planet\" — excluding Pluto and reclassifying it as a dwarf planet." },
];


</script>

<div class="planetsInfo-holder">
    {#each planetsInfo as {name, tilt, day, year, text}, i }

<IntersectionObserver let:intersecting top={-400}>
<div class="article-holder">
 <article class={`card card--${name} ${!intersecting ? "grey-filter" : ""}`}>
    <div class="card__planet">
      <div class="planet__atmosphere">
        <div class="planet__surface"></div>
      </div>
    </div>
    <div class="card__info">
      <h2 class="info__title">{name}</h2>
      <div class="info__form">
        <div class="info__item">
          <label class="info__label">tilt</label><span class="info__line"></span
          ><i class=" tilt__icon fas fa-long-arrow-alt-right"></i><span
            class="info__detail"
            >{tilt}&#176;
          </span>
        </div>
        <div class="info__item">
          <label class="info__label">day</label><span class="info__line"></span
          ><span class="info__detail">{day} hours</span>
        </div>
        <div class="info__item">
          <label class="info__label">year</label><span class="info__line"></span
          ><span class="info__detail">{year} days</span>
        </div>
      </div>
    </div>
  </article>
  <article>
    <div class={`info__item ${intersecting ? 'show' : 'hide'} `}>
      <p>
      {text}
      </p>
    </div>
  </article>
</div>
</IntersectionObserver>
    {/each}

</div>
