<template>
  <hgroup class="menu">
    <label><a href="./">Home</a></label>
    <label><a href="./games">Games</a></label>
    <label><a href="./about">About</a></label>
    <label><a href="./contact">Contact</a></label>
  </hgroup>
</template>

<style>


.menu {
  width: 1024px;
  justify-content: flex-end;
  margin-bottom: -50px;
  padding: 4px;
  z-index: 999;
}

.menu label {
  color: #000;
  font-size: 28px;
  margin: 10px 20px;
}

.menu label a {
  color: #ddd;
  font-size: 24px;
}

.menu label a:hover {
  color: #ccc !important;
  font-size: 24px;
  text-decoration: none;
}

</style>
