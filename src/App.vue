<template>
  <div><RegistrationPage /></div>
</template>

<script>
import RegistrationPage from "./components/RegistrationPage.vue";
export default {
  name: "App",
  components: { RegistrationPage },
};
</script>

<style>
html,
body {
  height: 100%;
  margin: 0;
  font-family: Lato, sans-serif;
}
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
