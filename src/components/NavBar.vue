<template>
  <div class="navbar">
    <div class="navbar__logo">
      <button>
        <img src="@/assets/icons/cube.png" alt="Logo" />
      </button>
    </div>
    <div class="navbar__menu-bar">
      <button class="for-mobile" @click="showingMenu = !showingMenu">
        <i class="fas fa-bars"></i>
      </button>

      <div class="navbar__menu" :class="{ 'show-menu': showingMenu }">
        <button class="btn explore">Explore</button>
        <button class="btn create">Create</button>
        <button class="btn wallet">Connect Wallet</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      showingMenu: false,
    };
  },
};
</script>

<style lang="scss" scoped>
@import "@/assets/scss/common/variables";
@import "@/assets/scss/common/mixins";
// @include debug(magenta);

.navbar {
  color: white;
  min-height: rem(60);
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 rem(20);
  background-color: #000;
  @include break-up(small) {
    min-height: rem(80);
  }

  &__logo {
    height: rem(40);
    button {
      height: 100%;
      background: none;
      outline: none;
      border: none;
      cursor: pointer;
      img {
        height: 100%;
      }
    }
  }

  &__menu-bar {
    > button {
      color: #fff;
      background: none;
      border: none;
      outline: none;
      font-size: rem(25);
      cursor: pointer;
    }
  }
  &__menu {
    position: fixed;
    right: -100%;
    top: rem(60);
    bottom: 0;
    padding: rem(20);
    display: flex;
    flex-direction: column;
    background-color: #292929;
    transition: all 0.4s ease-in-out;
    @include break-up(small) {
      position: initial;
      background: none;
      flex-direction: row;
      align-items: center;
      padding: 0;
    }

    button {
      font-size: rem(16);
      font-weight: 600;
      color: $gray;
      border: none;
      outline: none;
      line-height: 1;
      background: none;
      &:not(:last-child) {
        margin-bottom: rem(15);
      }
      @include break-up(small) {
        font-size: rem(17);
        &:not(:last-child) {
          margin-bottom: 0;
          margin-right: rem(40);
        }
      }
    }
    // .explore,
    // .create {
    //   position: relative;
    //   top: rem(8.5);
    // }
    .wallet {
      color: #000;
      padding: rem(15) rem(20);
      border-radius: rem(10);
      background-color: #fff;
      @include break-up(small) {
        padding: rem(18) rem(25);
      }
    }
  }
}
.show-menu {
  right: 0;
}
</style>