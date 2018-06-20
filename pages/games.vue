<template>
  <vgroup align="center">
    <app-menu/>
    <app-header/>
    <hgroup class="content">
      <vgroup class="game-list-item">
        <div class="splash">
            <img src="~/assets/images/canopy_crash_square.png">
            <a class="various" @click="showCanopy = true">~ Show More ~</a>
        </div>
        <vgroup class="description">
            <h3><img src="~/assets/images/canopy_crash_logo.png"></h3>
            <p>Our sophomore title release Canopy Crash All-Stars is a fun infinite scroller type game. Choose your character and see how far you can get!  The more leaves you collect the more points you get.  Canopy Crash is the perfect game for someone looking for a quick distraction.</p>
        </vgroup>
      </vgroup>
      <vgroup class="game-list-item">
          <div class="splash">
              <img src="~/assets/images/prymaries_square.png">
              <a class="various" @click="showPrymaries = true">~ Show More ~</a>
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
    <!--Canopy Crash Modal-->
    <app-modal v-if="showCanopy" @close="showCanopy = false">
       <carousel slot="screenshots" :per-page="1" :speed="1000" :loop="true" >
            <slide><img width="250" src="~/assets/images/CanopyCrashScreenshot_1.png" /></slide>
            <slide><img width="250" src="~/assets/images/CanopyCrashScreenshot_2.png" /></slide>
            <slide><img width="250" src="~/assets/images/CanopyCrashScreenshot_3.png" /></slide>
            <slide><img width="250" src="~/assets/images/CanopyCrashScreenshot_4.png" /></slide>
            <slide><img width="250" src="~/assets/images/CanopyCrashScreenshot_5.png" /></slide>
      </carousel>
      <h2 slot="header" style="color: #aaa; margin-bottom: 15px;">Canopy Crash Allstars</h2>
      <vgroup slot="body">
        <p>Canopy Crash Allstars is a infinite &ldquo;slider&rdquo; game available for Android and iOS. Players takes control of a &ldquo;crasher&rdquo; as they slide faster and faster down the infinite &ldquo;Forever Tree&rdquo; collecting leaves and power-ups while avoiding obstacles at increasingly breakneck speeds.</p>
        <ul style="padding-left: 14px;">
            <li>6 unlockable &ldquo;Crashers&rdquo; to pick from: Koalas to Dinosaurs; each with their own unique animations.</li>
            <li>Unique Handpainted art and aesthetic.</li>
            <li>An infinitely randomized tree. Never slide the same tree twice.</li>
            <li>Connect on Facebook and compare your hi-score against friends.</li>
            <li>Free on Android and iOS</li>
        </ul>
      </vgroup>
      <span slot="release">12/24/2014</span>
    </app-modal>
    <!--Prymaries Modal-->
    <app-modal v-if="showPrymaries" @close="showPrymaries = false">
       <carousel slot="screenshots" :per-page="1" :speed="1000" :loop="true" >
           <slide><img width="250" src="~/assets/images/prymaries_splash.png"></slide>
            <slide><img width="250" src="~/assets/images/android_home.png" /></slide>
            <slide><img width="250" src="~/assets/images/android_game.png" /></slide>
            <slide><img width="250" src="~/assets/images/android_how.png" /></slide>
            <slide><img width="250" src="~/assets/images/android_level.png" /></slide>
      </carousel>
      <h2 slot="header" style="color: #aaa; margin-bottom: 15px;">Prymaries</h2>
      <vgroup slot="body">
        <p>The World is full of colorful characters...now merge them together and make them explode! Prymaries is a color based match 3 game. Combine primary colored blocks (yellow, red, and blue) together to form secondary colored blocks (purple, orange, and green) 3+ adjacent secondary blocks explode in a blaze of pigment and glory! Fun and fast with an easy to learn mechanic, Prymaries is the perfect app for the puzzle addict in us all. </p>
        <ul style="padding-left: 14px;">
            <li>Color based matching madness</li>
            <li>More blocks means more points, larger chains and combos rack in the bonus points.</li>
            <li>3 amazing game modes to try: Original for near endless matching fun, Time attack is a race against the clock for pigment supremacy, and Puzzle mode with 30+ brain stumping levels.</li>
            <li>Leaderboards let you brag to your friends and the world, about your color mixing skills!</li>
        </ul>
      </vgroup>
      <span slot="release">12/12/2012</span>
    </app-modal>
  </vgroup>

</template>

<script>
import AppHeader from "~/components/AppHeader.vue";
import AppMenu from "~/components/AppMenu.vue";
import AppFooter from "~/components/AppFooter.vue";
import AppModal from "~/components/AppModal.vue";

export default {
  components: {
    AppHeader,
    AppMenu,
    AppFooter,
    AppModal
  },
  data() {
    return {
      showCanopy: false,
      showPrymaries: false
    }
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
