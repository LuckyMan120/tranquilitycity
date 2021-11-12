<template>
  <div class="hero">
    <!-- Youtube Video -->
    <div class="hero__yt-vid">
      <iframe
        width="560"
        height="315"
        src="https://www.youtube.com/embed/5dXv5dU3fXk"
        title="YouTube video player"
        frameborder="0"
        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
        allowfullscreen
      ></iframe>

      <!-- Down part -->
      <div class="down-part">
        <div class="info">
          <div class="name">
            <div>Shamanka:</div>
            <div>The Healer</div>
          </div>
          <div class="type">World of Umans</div>
        </div>
        <div class="button">
          <button>Go to auction</button>
        </div>
      </div>
    </div>

    <!-- Intro -->
    <div class="hero__intro">
      <h1 class="title">Trade without platform fees on Artion</h1>
      <p class="desc-1">
        Artion is an NFT marketplace built on Fantom. Create and trade NFTs
        instantly with low network costs.
      </p>
      <p class="desc-2">
        Warning: This is a beta version. Use at your own caution.
      </p>
      <div class="explore-btn">
        <button>Explore</button>
      </div>
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

.hero {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
  color: #fff;
  padding: rem(100) rem(20) rem(40) rem(20);
  background-color: #000;
  @include break-up(small) {
    flex-direction: row;
  }

  /**** yt video ****/
  &__yt-vid {
    width: calc(100% - rem(20));
    min-height: rem(380);
    display: grid;
    grid-template-rows: auto auto;
    padding: rem(10) rem(10);
    border-radius: rem(20);
    box-shadow: rgba(255, 255, 255, 0.342) 0px 10px 36px 0px,
      rgba(0, 0, 0, 0.06) 0px 0px 0px 1px;
    @include break-up(small) {
      order: 2;
      width: rem(540);
      min-height: rem(620);
      padding: rem(20) rem(20);
      margin-left: rem(80);
    }

    iframe {
      // @include debug(magenta);
      width: 100%;
      @include break-up(small) {
        height: rem(482);
      }
    }

    .down-part {
      // @include debug(magenta);
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin: 0 rem(15) 0 rem(15);

      .info {
        display: flex;
        font-size: rem(12);
        @include break-up(small) {
          font-size: rem(16);
        }

        .name {
          color: $gray;
        }

        .type {
          width: rem(80);
          margin-left: rem(10);
          font-weight: 700;
        }
      }

      .button {
        button {
          border: none;
          outline: none;
          color: #fff;
          padding: rem(5) rem(10);
          font-weight: 700;
          background-color: $blue;
          border-radius: rem(5);
          @include break-up(small) {
            font-size: rem(16);
            padding: rem(15) rem(24);
            border-radius: rem(8);
          }
        }
      }
    }
  }

  /**** intro ****/
  &__intro {
    @include break-up(small) {
      order: 1;
      width: rem(540);
      margin-right: rem(80);
    }
    .title {
      text-align: center;
      font-size: rem(40);
      margin-bottom: rem(10);
      @include break-up(small) {
        text-align: left;
        font-size: rem(50);
        margin-bottom: rem(16);
      }
    }
    .desc-1,
    .desc-2 {
      text-align: center;
      font-weight: 600;
      color: $gray;
      font-size: rem(12);
      @include break-up(small) {
        text-align: left;
        font-size: rem(15);

        &:not(:last-child) {
          margin-bottom: rem(15);
        }
      }
    }
    .explore-btn {
      text-align: center;
      margin-top: rem(25);
      @include break-up(small) {
        text-align: left;
        margin-top: rem(24);
      }
      button {
        background-color: $blue;
        color: #fff;
        border: none;
        outline: none;
        font-weight: 700;
        padding: rem(14) rem(50);
        border-radius: rem(10);
        @include break-up(small) {
          padding: rem(15) rem(53);
          font-size: rem(16);
        }
      }
    }
  }
}
</style>