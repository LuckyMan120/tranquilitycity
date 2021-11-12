<template>
  <div id="app">
    <NavBar class="navbar-app" />
    <router-view />
  </div>
</template>

<script>
import NavBar from "@/components/NavBar.vue";

export default {
  components: {
    NavBar,
  },
};
</script>

<style lang="scss">
@import "@/assets/scss/common/variables";
@import "@/assets/scss/common/mixins";
/***** Global *****/
* {
  box-sizing: border-box;
}
html,
body {
  margin: 0;
  padding: 0;
  font-family: $montserrat;
}
/***** /Global *****/

.app {
}
.navbar-app {
  position: fixed;
  top: 0;
  right: 0;
  left: 0;
}
</style>
