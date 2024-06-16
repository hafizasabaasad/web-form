<template>
  <Signupform />
</template>

<script>

// with background image
import Signupform from "./components/Signupform-background.vue";
// with 2 columns display
// import Signupform from "./components/Signupform-side-by-side.vue";

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
body {
display: grid;
min-height: 0;
grid-template-rows: 1fr;
grid-template-columns: 1fr; /* 1 columns */

}
html {
display: grid;
height: 100%; /* OR min-height: 100% */
}

</style>
