<template>
  <div class="home">
    <Hero />
    <SecondSec />
  </div>
</template>

<script>
// @ is an alias to /src
import Hero from "@/components/home/Hero.vue";
import SecondSec from "@/components/home/SecondSec.vue";

export default {
  name: "Home",
  components: {
    Hero,
    SecondSec,
  },
};
</script>

<style lang="scss" scoped>
@import "@/assets/scss/common/mixins";

.home {
}
</style>