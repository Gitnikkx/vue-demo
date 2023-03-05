<template>
  <div style="margin: 80px">
    <h1>Discover healthy living</h1>
    <div class="flexButtons">
      <p class="flex-p">Calcium 101</p>
      <p class="flex-p">Vitamins for women</p>
      <p class="flex-p">Immunity and Strength</p>
    </div>

    <div style="display: flex;justify-content: right;gap: 20px;margin-bottom: 10px;">
      <button @click="showPrev" class="slideBtn">
        <img class="left-arrow" src="../public/assets/right-arrow.svg" />
      </button>

      <button @click="showNext" class="slideBtn">
        <img src="../public/assets/right-arrow.svg" />
      </button>
    </div>

    <VueSlickCarousel
      ref="carousel"
      :slidesToShow="2"
      :variableWidth="true"
      :infinite="true"
      :arrows="false"
    >
      <SliderBox />
      <SliderBox />
      <SliderBox />
    </VueSlickCarousel>

    <div class="explore-btn">
      <p class="explore-font">EXPLORE MORE BLOGS</p>
    </div>
  </div>
</template>

<script>
import SliderBox from "./SliderBox.vue";
import VueSlickCarousel from "vue-slick-carousel";
import "vue-slick-carousel/dist/vue-slick-carousel.css";

export default {
  name: "DiscoverS",
  components: {
    SliderBox,
    VueSlickCarousel,
  },
  methods: {
    showNext() {
      this.$refs.carousel.next();
    },
    showPrev() {
      this.$refs.carousel.prev();
    },
  },
};
</script>

<style scoped>
.flexButtons {
  display: flex;
}
.flex-p {
  width: fit-content;
  background: #11f7bb;
  border-radius: 25px;
  padding: 10px 20px 10px 20px;
  font-size: 14px;
  font-weight: 700;
  color: #121d64;
  margin-right: 16px;
  cursor: pointer;
  align-items: center;
}
.slideBtn {
  width: 64px;
  height: 40px;
  border: 1px solid #121d64;
  border-radius: 26.5px;
  cursor: pointer;
}
.left-arrow {
  transform: rotate(180deg);
}
.explore-btn {
  width: fit-content;
  height: 48px;
  background: #121d64;
  border-radius: 4px;
  cursor: pointer;
  margin-top: 40px;
}
.explore-font {
  font-weight: 900;
  font-size: 14px;
  color: #f0f0f0;
  padding: 13px;
}
</style>
