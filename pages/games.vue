<template>
  <vgroup align="center">
    <app-menu/>
    <app-header/>
    <hgroup class="content">
      <vgroup class="game-list-item">
        <div class="splash">
            <img src="~/assets/images/canopy_crash_square.png">
            <a class="various" data-fancybox-type="iframe" href="./canopycrash_preview.html">~ Show More ~</a>
        </div>
        <vgroup class="description">
            <h3><img src="~/assets/images/canopy_crash_logo.png"></h3>
            <p>Our sophomore title release Canopy Crash All-Stars is a fun infinite scroller type game. Choose your character and see how far you can get!  The more leaves you collect the more points you get.  Canopy Crash is the perfect game for someone looking for a quick distraction.</p>
        </vgroup>
      </vgroup>
      <vgroup class="game-list-item">
          <div class="splash">
              <img src="~/assets/images/prymaries_square.png">
              <a class="various" data-fancybox-type="iframe" href="./prymaries_preview.html">~ Show More ~</a>
          </div>
          <vgroup class="description">
              <h3><img src="~/assets/images/prymaries_logo.png"></h3>
              <p>The World is full of colorful characters...now merge them together and make them explode! Prymaries is a color based match 3 game. Combine primary colored blocks (yellow, red, and blue) together to form secondary colored blocks (purple, orange, and green) 3+ adjacent secondary blocks explode in a blaze of pigment and glory! Fun and fast with an easy to learn mechanic, Prymaries is the perfect app for the puzzle addict in us all.</p>
          </vgroup>
      </vgroup>
      <vgroup class="game-list-item">
          <div>
              <img src="~/assets/images/penguins_square.png">
          </div>
          <vgroup class="description">
              <h3><img src="~/assets/images/ArticRUSH_LOGO.png"></h3>
              <p style="text-align:center;">Coming Soon!</p>
          </vgroup>
      </vgroup>
  </hgroup>
    <app-footer/>
  </vgroup>
</template>

<script>
import AppHeader from "~/components/AppHeader.vue";
import AppMenu from "~/components/AppMenu.vue";
import AppFooter from "~/components/AppFooter.vue";

export default {
  components: {
    AppHeader,
    AppMenu,
    AppFooter
  }
};
</script>

<style>
.content {
  background: #000;
  width: 1024px;
  min-height: 100%;
  box-shadow: -5px 0px 10px 0px rgba(0, 0, 0, .3);
}



.game-list {
  width: 800px;
  -webkit-box-pack: center;
}

.game-list-item {
  width: 32%;
  padding: 10px;
}

.game-list-item vgroup {
  -webkit-box-align: start;
}

.game-list-item .description {
  padding: 5px;
}

.game-list-item h3 {
  text-align: center;
  width: 100%;
}

.game-list-item h3 img {
  width: 300px;
}

.game-list-item p {
  color: #ddd;
  font-size: 14px;
  padding: 5px 10px;
  width: 100%;
}

.splash {
  position: relative;
}

.game-list-item .splash:hover img {
  opacity: 0.2;
  transition: opacity 0.3s;
}

.game-list-item a {
  display: none;
  color: #9e0b0f !important;
  font-size: 28px;
  font-weight: 600;
  width: 100%;
  height: 100%;
  text-align: center;
  text-decoration: none;
  position: absolute;
  top: 0;
  line-height: 270px;
}

.game-list-item .splash:hover a {
  display: block;
  text-decoration: none;
}

</style>
