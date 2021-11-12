<template>
  <div class="single-why">
    <div class="image">
      <img src="@/assets/icons/circle.png" alt="circle" />
    </div>

    <div class="info">
      <div class="title">Easy Connect</div>
      <p class="desc">
        Using Metamask or CoinBase Wallet. Just click "Connect Wallet" on the
        top right to start.
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
// @include debug(magenta);
// @include break-up(small){}

.single-why {
  box-shadow: rgba(99, 99, 99, 0.2) 0px 2px 8px 0px;
  width: rem(283);
  border-radius: rem(25);
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: rem(20);
  margin-bottom: rem(20);
  @include break-up(small) {
    margin-bottom: rem(0);
    padding: rem(30);
    &:not(:last-child) {
      margin-right: rem(20);
    }
  }

  .image {
    width: rem(102);
    height: rem(102);
    margin-bottom: rem(25);
    display: flex;
    justify-content: center;
    align-items: center;
    border-radius: 50%;
    box-shadow: rgba(149, 157, 165, 0.2) 0px 8px 24px;
    @include break-up(small) {
      margin-bottom: rem(45);
    }

    img {
      width: rem(82);
      height: rem(82);
    }
  }

  .info {
    .title {
      font-weight: 700;
      font-size: rem(14);
      text-align: center;
      @include break-up(small) {
        font-size: rem(20);
      }
    }
    .desc {
      font-size: rem(12);
      text-align: center;
      @include break-up(small) {
        font-size: rem(14);
      }
    }
  }
}
</style>