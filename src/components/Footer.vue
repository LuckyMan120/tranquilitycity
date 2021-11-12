<template>
  <div class="footer">
    <div class="logo">
      <img src="@/assets/icons/cube.png" alt="logo" /> Artion
    </div>
    <div class="links">
      <router-link to="#">Privacy Policy</router-link>
      <router-link to="#">Cookie Policy</router-link>
      <router-link to="#">Terms of Service</router-link>
    </div>
    <div class="logo-2">
      <img src="@/assets/icons/cube.png" alt="logo" /> fantom
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
@import "@/assets/scss/common/variables";
@import "@/assets/scss/common/mixins";
// @include debug(magenta);

.footer {
  height: rem(128);
  background-color: $blue;
  color: #fff;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-around;
  @include break-up(small) {
    height: rem(144);
    flex-direction: row;
  }

  .logo,
  .logo-2 {
    font-size: rem(30);
    display: flex;
    align-items: center;
    font-weight: 500;
    @include break-up(small) {
      font-size: rem(35);
    }
    img {
      height: rem(32);
      margin-right: rem(5);
      @include break-up(small) {
        height: rem(35);
      }
    }
  }
  .links {
    a {
      color: #fff;
      font-size: rem(14);
      font-weight: 600;
      &:not(:last-child) {
        margin-right: rem(12);
      }
      @include break-up(small) {
        font-size: rem(18);
        &:not(:last-child) {
          margin-right: rem(35);
        }
      }
    }
  }
}
</style>