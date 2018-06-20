<template>
  <vgroup align="center">
    <app-menu/>
    <app-header/>
    <vgroup class="content">
      <vgroup class="banner">
        <carousel :per-page="1" :speed="1000" :loop="true" >
          <slide>
             <a class="various" data-fancybox-type="iframe" href="http://www.youtube.com/embed/Trz_P0bGyw8">
                <img src="~/assets/images/CanopyCrashFeature.png" width="100%">
            </a>
            <hgroup class="market" align="center">
              <a href="https://itunes.apple.com/us/app/canopy-crash-allstars/id955075315?ls=1&mt=8"><img src="~/assets/images/available_ios.png" /></a>
              <a href="https://play.google.com/store/apps/details?id=net.heightadvantage.canopycrash"><img src="~/assets/images/available_market.png" /></a>
            </hgroup>
          </slide>
          <slide>
            <a class="various" data-fancybox-type="iframe" href="http://www.youtube.com/embed/QJyKlAkpfig">
                <img src="~/assets/images/PrymariesSuperBanner.jpg" width="100%">
            </a>
            <hgroup class="market" align="center">
              <a href="https://itunes.apple.com/us/app/prymaries-free/id571493571?ls=1&mt=8"><img src="~/assets/images/available_ios.png" /></a>
              <a href="https://play.google.com/store/apps/details?id=air.net.heightadvantage.prymaries"><img src="~/assets/images/available_market.png" /></a>
            </hgroup>
          </slide>
        </carousel>


        <!-- <h1>Prymaries Now Available (IOS/Android)</h1> -->
       </vgroup>
    </vgroup>
    <app-footer/>
  </vgroup>
</template>

<script>
import AppHeader from '~/components/AppHeader.vue'
import AppMenu from '~/components/AppMenu.vue'
import AppFooter from '~/components/AppFooter.vue'

export default {
  components: {
    AppHeader,
    AppMenu,
    AppFooter
  }
}
</script>

<style>
  h1 {
    color: #fff;
  }

  .content {
    background: #000;
    width: 1024px;
    min-height: 100%;
    box-shadow: -5px 0px 10px 0px rgba(0, 0, 0, .3);
  }

  video {
    margin-bottom: 15px;
  }

  .videoholder {
    background: #75a3dc;
    margin-bottom: 20px;
    -webkit-box-shadow: 7px 7px 5px rgba(50, 50, 50, 0.3);
    -moz-box-shadow: 7px 7px 5px rgba(50, 50, 50, 0.3);
    box-shadow: 7px 7px 5px rgba(50, 50, 50, 0.3);
  }

  .banner h2 {
    width: 100%;
  }

  .banner label {
    margin: 5px;
    color: #9e0b0f;
    font-size: 24px;
  }

  .market img {
    padding: 5px;
  }

</style>
