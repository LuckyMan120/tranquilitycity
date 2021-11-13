<template>
  <div class="sec-2">
    <!-- Why Artion -->
    <div class="sec-2__why">
      <h1>Why Artion</h1>
      <div class="all-whys">
        <SingleWhy v-for="(why, index) in 4" :key="index" />
      </div>
    </div>

    <!-- Browse by category -->
    <div class="sec-2__browse">
      <h1>
        Browse by <br />
        category
      </h1>
      <div class="categories">
        <Category v-for="(cate, index) in 8" :key="index" />
      </div>
    </div>
  </div>
</template>

<script>
import SingleWhy from "@/components/utilities/SingleWhy.vue";
import Category from "@/components/utilities/Category.vue";
export default {
  components: {
    SingleWhy,
    Category,
  },
};
</script>

<style lang="scss" scoped>
@import "@/assets/scss/common/variables";
@import "@/assets/scss/common/mixins";
// @include debug(magenta);
// @include break-up(small){}

.sec-2 {
  padding-top: rem(40);
  @include break-up(small) {
    padding-top: rem(120);
  }
  &__why {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-bottom: rem(100);
    @include break-up(small) {
      margin-bottom: rem(190);
    }
    > h1 {
      text-align: center;
      font-size: rem(35);
      margin-bottom: rem(35);
      @include break-up(small) {
        font-size: rem(50);
        margin-bottom: rem(100);
      }
    }
    .all-whys {
      display: flex;
      gap: rem(20);
      flex-wrap: wrap;
      justify-content: center;
    }
  }
  &__browse {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-bottom: rem(100);
    > h1 {
      text-align: center;
      margin-bottom: rem(35);
      @include break-up(small) {
        font-size: rem(50);
        margin-bottom: rem(100);
      }
    }

    .categories {
      @include break-up(small) {
        max-width: rem(1200);
        display: flex;
        flex-wrap: wrap;
        gap: rem(35);
        justify-content: center;
      }
    }
  }
}
</style>