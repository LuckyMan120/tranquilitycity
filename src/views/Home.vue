<template>
  <div class="home">
    <Hero />
  </div>
</template>

<script>
// @ is an alias to /src
import Hero from "@/components/home/Hero.vue";

export default {
  name: "Home",
  components: {
    Hero,
  },
};
</script>

<style lang="scss" scoped>
@import "@/assets/scss/common/mixins";

.home {
}
</style>