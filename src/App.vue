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
  font-family: "Lato", sans-serif;
  line-height: 1.5;
}

p {
  margin-block-start: 0;
  margin-block-end: 0;
}
:root {
  --black: black;
  --dark-grey: #333;
  --blue1: #1075ab;
  --white: white;
  --grey1: #f4f4f4;
  --steel-blue: rgba(18, 134, 191, 0.2);
}
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
