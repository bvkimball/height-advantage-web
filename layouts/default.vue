<template>
  <div>
    <nuxt/>
  </div>
</template>

<style>
html {
  font-family: "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

*, *:before, *:after {
  box-sizing: border-box;
  margin: 0;
}

body {
  /*background: #000 !important;*/
  font-family: "Open Sans", sans-serif;
  background: #333 url("~/assets/images/background.png");
  font-weight: lighter;
  line-height: 24px;
}

a {
  color: #fff !important;
  text-decoration: none;
}
a:hover {
  text-decoration: underline;
}

hgroup, vgroup {
  display: flex;
}
hgroup {
  flex-flow: row nowrap;
}
vgroup {
  flex-flow: column;
}
vgroup[align="center"] {
    align-items: center;  
}
hgroup[align="center"] {
    justify-content: center;  
}

group > row:first-of-type {
  min-width: 200px;
}


</style>
