<template>
  <hgroup class="header">
      <div class="logo">
          <img src="~/assets/images/slimlogo.png" width="220"/>
      </div>
  </hgroup>
</template>

<style>

.header {
  -webkit-box-pack: center;
  background: #9e0b0f url("~/assets/images/website_header.png") no-repeat;
  width: 1024px;
  height: 180px;
  background-position-y: 30px;
  box-shadow: -5px 0px 10px 0px rgba(0, 0, 0, .3);
}

.header::before {
  content: "";
  position: absolute;
  z-index: -1;
  top: 0px;
  width: 15px;
  height: 100%;

}

.logo {
  padding: 10px 40px;
}


</style>
