<template>
  <vgroup align="center">
    <app-menu/>
    <app-header/>
    <vgroup class="content" align="center">
      <h2 style="color: #fff;">&nbsp;</h2>
      <div class="about">
          <p>Height Advantage Games was founded in 2011 by two brothers with an intense desire to stop talking about making a game company, and just do it already. Beginning in November 2011 the pair began work on their initial offering Prymaries, and created a backlog of amazing ideas that they can not wait to show to the world.</p>
      </div>
      <hgroup class="bio" align="center">
        <img class="bio-pic" src="~/assets/images/pic_chris.png"/>
        <div class="bio-about">
          <h2>Chris Kimball</h2>
          <p>Determined to Art from an early age, Chris has undergone an intensive training routine of holding a pencil and making marks on paper... alot! Although after a tragic accident involving a pad of bristol board and some Sharpies left 17 dead, Chris learned that he must only use his powers of Art for good (and profit). Currently Chris wages war on the forces of darkness as the world's only freelance, giant, crime-solving, (martial) artist.<br><br>Check out Chris's Artwork @ <a href="http://chrislkimball.com">www.chrislkimball.com</a></p>
        </div>
      </hgroup>
      <hgroup class="bio" align="center">
        <img class="bio-pic" src="~/assets/images/pic_brian.png"/>
        <div class="bio-about">
          <h2>Brian Kimball</h2>
          <p>Born with the desire to make amazing games, Brian has honed all of his skills to exceed at this one task. Now a seasoned game developer, Brian's only goal is to make the best games possible.</p>
        </div>
      </hgroup>
    </vgroup>
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


.about {
  width: 800px;
  color: #ddd;
}


.bio {
  width: 100%;
  margin: 10px;
  color: #fff;
}

.bio-pic {
  border-radius: 20%;
  margin-top: 20px;
  width: 150px;
  height: 150px;
}

.bio-about {
  width: 600px;
  padding: 20px;
  text-align: left;
}


</style>
