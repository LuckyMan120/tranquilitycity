<template>
  <div class="navbar">
    <div class="navbar__logo">
      <button>
        <img src="@/assets/icons/cube.png" alt="Logo" />
      </button>
    </div>
    <div class="navbar__menu-bar">
      <button>
        <i class="fas fa-bars"></i>
      </button>
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

.navbar {
  // @include debug(yellow);
  color: white;
  min-height: rem(60);
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 rem(20);
  background-color: #000;

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
    button {
      color: #fff;
      background: none;
      border: none;
      font-size: rem(25);
      cursor: pointer;
    }
  }
}
</style>