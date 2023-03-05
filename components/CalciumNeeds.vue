<template>
  <div>
    <h1 style="text-align: center">
      Choose Shelcal 500 to fulfill your calcium needs
    </h1>
    <div class="gridSection">
      <div class="textGrid">
        <div v-for="item in list" :key="item.id">
          <ContentBoxVue :srcImg="item.src" :title="item.text" />
        </div>
      </div>

      <img class="imgCal" src="../public/assets/pill-cal.svg" />

      <div class="textGrid">
        <div v-for="item in list2" :key="item.id">
          <ContentBoxVue :srcImg="item.src" :title="item.text" />
        </div>
      </div>
    </div>
  </div>
</template>


<script>
import ContentBoxVue from "./ContentBox.vue";

export default {
  name: "NeedS",
  components: {
    ContentBoxVue,
  },
  props: {
    list: {
      type: Array,
      default: () => [
        {
          id: 0,
          text: "Optimises Calcium absorption",
          src: "https://picsum.photos/200",
        },
        {
          id: 1,
          text: "Improves muscle strength",
          src: "https://picsum.photos/100",
        },
      ],
    },
    list2: {
      type: Array,
      default: () => [
        {
          id: 0,
          text: "Helps in boosting immunity",
          src: "https://picsum.photos/200",
        },
        {
          id: 1,
          text: "Increases bone density",
          src: "https://picsum.photos/100",
        },
      ],
    },
  },
};
</script>


<style scoped>
.gridSection {
  display: grid;
  grid-template-columns: 315px 345px 315px;
  gap: 47px;
  width: fit-content;
  margin: auto;
}

.imgCal {
  width: 345px;
  height: 536px;
}
.textGrid {
  display: grid;
  grid-template-areas: 1fr;
}
</style>