<template>
  <div id="app">
    <NavBar class="navbar-app" />
    <router-view />
    <Footer class="footer-app" />
  </div>
</template>

<script>
import NavBar from "@/components/NavBar.vue";
import Footer from "@/components/Footer.vue";

export default {
  components: {
    NavBar,
    Footer,
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
a {
  text-decoration: none;
}
// ---- Utility classes ----
.for-mobile {
  @include break-up(small) {
    display: none;
  }
}
.for-pc {
  @include break-down(small) {
    display: none;
  }
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
