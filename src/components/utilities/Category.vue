<template>
  <div class="single-why">
    <div class="image">
      <img src="@/assets/icons/teddy-bear.png" alt="circle" />
    </div>

    <div class="button">
      <h2>Cate</h2>
      <button><i class="fas fa-chevron-right"></i></button>
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

.single-why {
  box-shadow: rgba(99, 99, 99, 0.2) 0px 2px 8px 0px;
  width: rem(283);
  border-radius: rem(25);
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: rem(30) rem(10) rem(20) rem(10);
  margin-bottom: rem(30);
  @include break-up(small) {
    margin-bottom: rem(0);
  }

  .image {
    width: rem(102);
    height: rem(102);
    margin-bottom: rem(40);
    display: flex;
    justify-content: center;
    align-items: center;
    border-radius: 50%;
    box-shadow: rgba(149, 157, 165, 0.2) 0px 8px 24px;

    img {
      width: rem(82);
      height: rem(82);
    }
  }

  .button {
    // @include debug(magenta);
    width: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: rem(2);
    background-color: $light-gray;
    border-radius: rem(40);

    h2 {
      font-size: rem(14);
      line-height: rem(14);
      margin-left: rem(12);
    }

    button {
      width: rem(33);
      height: rem(33);
      color: #fff;
      border-radius: 50%;
      font-size: rem(12);
      border: none;
      outline: none;
      background-color: $blue;
      margin-right: rem(2);
    }
  }
}
</style>