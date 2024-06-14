<template>
  <Signupform />
</template>

<script>
import Signupform from "./components/Signupform.vue";

export default {
  name: "App",
  components: { Signupform },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #010104;
  margin-top: auto;
}
body,
html {
  height: 100%;
  margin-top: 0px;
  margin-bottom: 0px;
}

body {
  margin: auto;
  margin-bottom: 0px;
  background: white;
}
</style>
