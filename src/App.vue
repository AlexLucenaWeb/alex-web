<template>
  <the-header></the-header>
  <div class="app__bg-back">
    <div class="app__bg-front"></div>
    <div class="app__bg-botton"></div>
  </div>
  <logo-animation></logo-animation>
  <bio-sec></bio-sec>
</template>

<script>
import LogoAnimation from "./components/sections/AnimationSection.vue";
import BioSec from "./components/sections/BioSection.vue";
import TheHeader from "./components/layout/TheHeader.vue";

export default {
  components: {
    TheHeader,
    LogoAnimation,
    BioSec,
  },
};
</script>

<style>
@font-face {
  font-family: jeko;
  src: url("../public/fonts/Jeko-Extra-Bold.ttf"),
    url("../public/fonts/Jeko-Regular.ttf"),
    url("../public/fonts/Jeko-Light.ttf");
}
body {
  margin: 0;
}
#app {
  font-family: jeko, sans-serif;
  /* font-weight: normal; */
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
.bapp__bg-back {
  position: fixed;
  z-index: -2;
  top: 0;
  right: 0;
  width: 100vw;
  height: 100vh;
  background-color: white;
}
.app__bg-front {
  position: fixed;
  z-index: -1;
  top: 50px;
  left: 50px;
  width: calc(100vw - 117px);
  height: calc(100vh - 100px);
  background-color: #ff5851;
}
.app__bg-botton {
  position: fixed;
  z-index: 999;
  bottom: 0;
  right: 0;
  width: 100vw;
  height: 50px;
  background-color: white;
}

/* --- SECTIONS  --- */
section {
  width: calc(100vw - 117px);
  min-height: calc(100vh - 100px);
  margin: 50px 0 0 50px;
}
</style>
