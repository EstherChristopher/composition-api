<template>
  <HelloWorld msg="Welcome to Your Vue.js App" />
  <SettingsProvider>
    <ThemeButton />
  </SettingsProvider>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import SettingsProvider from "./components/SettingsProvider.vue";
import ThemeButton from "./components/ThemeButton.vue";

export default {
  name: "App",
  components: {
    HelloWorld,
    SettingsProvider,
    ThemeButton
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
