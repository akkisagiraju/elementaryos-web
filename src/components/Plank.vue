<template>
  <div class="plank">
    <div class="plank__apps-container">
      <div class="plank-app" :key="app.name" v-for="app in apps">
        <span class="plank-app__name" v-if="app.name === highlightedApp.name">{{
          highlightedApp.name
        }}</span>
        <img
          class="plank-app__icon"
          :src="app.icon"
          @mouseenter="() => setHighlightedApp(app)"
          @mouseleave="resetHighlightedApp"
        />
      </div>
    </div>
    <div class="plank__base" />
  </div>
</template>

<script>
export default {
  name: "Plank",
  data() {
    return {
      highlightedApp: {},
      apps: [
        { name: "Files", icon: require("../assets/icons/files.svg") },
        { name: "Epiphany", icon: require("../assets/icons/epiphany.svg") },
        { name: "Calendar", icon: require("../assets/icons/calendar.svg") },
        { name: "Music", icon: require("../assets/icons/music.svg") },
        { name: "Videos", icon: require("../assets/icons/videos.svg") },
        { name: "Photos", icon: require("../assets/icons/photos.svg") },
        {
          name: "System Settings",
          icon: require("../assets/icons/settings.svg"),
        },
        { name: "AppCenter", icon: require("../assets/icons/appcenter.svg") },
      ],
    };
  },
  methods: {
    setHighlightedApp(app) {
      this.highlightedApp = app;
    },
    resetHighlightedApp() {
      this.highlightedApp = {};
    },
  },
};
</script>


<style scoped>
.plank {
  position: absolute;
  width: max-content;
  left: 50%;
  bottom: 0;
  transform: translate(-50%);
}

.plank__apps-container {
  display: flex;
  justify-content: center;
  margin-bottom: -20px;
  position: relative;
}

.plank-app {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.plank-app__name {
  color: white;
  background-color: #2d2d2d;
  display: inline-block;
  position: absolute;
  bottom: 64px;
  padding: 4px;
  font-size: 1.25em;
}

.plank-app__icon {
  height: 48px;
  width: 48px;
  margin: 0 6px;
}

.plank__base {
  background-color: #ced2d5;
  border-top-left-radius: 4px;
  border-top-right-radius: 4px;
  height: 25px;
}
</style>