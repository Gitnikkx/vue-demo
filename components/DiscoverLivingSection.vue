<template>
  <div style="margin: 80px">
    <h1>{{ data[0].blog_section_title }}</h1>
    <div class="flexButtons">
      <div v-for="item in list" :key="item.id">
        <p class="flex-p">{{ item.tag }}</p>
        <!-- <p class="flex-p">Vitamins for women</p>
      <p class="flex-p">Immunity and Strength</p> -->
      </div>
    </div>

    <div class="arrow-css">
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
      <div v-for="item in list" :key="item.id">
        <SliderBox :heading="item.text" :tag="item.tag" :imgSrc="item.src" />
      </div>
    </VueSlickCarousel>

    <div class="explore-btn">
      <p class="explore-font">{{ data[0].blog_cta.cta_title }}</p>
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
  props: {
    data: {
      type: Array,
    },
    list: {
      type: Array,
      default: () => [
        {
          id: 0,
          text: "Trust calcium supplements to help fill your nutritional gap",
          tag: "Calcium 101",
          src: "https://picsum.photos/200",
        },
        {
          id: 1,
          text: "The Story of Your Bones: Calcium at Every Age",
          tag: "Vitamins for women",
          src: "https://picsum.photos/400",
        },
        {
          id: 2,
          text: "Vitamin D: What do you need to know",
          tag: "Calcium 101",
          src: "https://picsum.photos/600",
        },
        {
          id: 3,
          text: "Vitamin D",
          tag: "Calcium 101",
          src: "https://picsum.photos/900",
        },
        {
          id: 4,
          text: "Vitamin A:",
          tag: "Vitamins for women",
          src: "https://picsum.photos/800",
        },
      ],
    },
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
  overflow: auto;
}

.arrow-css {
  display: flex;
  justify-content: right;
  gap: 20px;
  margin-bottom: 10px;
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
