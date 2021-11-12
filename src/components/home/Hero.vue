<template>
  <div class="hero">
    <div class="hero__yt-vid"></div>
    <div class="hero__intro">
      <h1 class="title">Trade without platform fees on Artion</h1>
      <p class="desc-1">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Beatae possimus
        sed velit dolores necessitatibus quis inventore voluptatem dolorum
        exercitationem excepturi?
      </p>
      <p class="desc-2">
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Nisi
        laudantium ipsum optio?
      </p>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
@import "@/assets/scss/common/variables";
@import "@/assets/scss/common/mixins";
.hero {
  // @include debug(red);
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  color: #fff;
  padding: 0 rem(20);
  background-color: #000;

  &__intro {
    .title {
      text-align: center;
      font-size: rem(45);
      margin-bottom: rem(10);
    }
    .desc-1,
    .desc-2 {
      text-align: center;
    }
  }
}
</style>