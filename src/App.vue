<template>
  <div id="app">
    <wingpanel />
    <plank />
  </div>
</template>

<script>
import "@fontsource/inter";
import "@fontsource/inter/500.css";
import "@fontsource/inter/700.css";

import Wingpanel from "./components/Wingpanel";
import Plank from "./components/Plank.vue";

export default {
  name: "App",
  components: { Wingpanel, Plank },
};
</script>

<style>
body {
  margin: 0;
  padding: 0;
  font-family: Inter;
  background: url("./assets/wallpaper.jpg");
  background-repeat: no-repeat;
  background-size: cover;
  font-size: 10px;
}

#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
