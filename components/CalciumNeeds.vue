<template>
  <div>
    <h1 style="text-align: center">
      {{ data[0]?.title_text?.text }}
    </h1>
    <div class="gridSection">

      <div class="textGrid">
        <div v-for="item in data" :key="item.id">
          <ContentBoxVue :srcImg="item.pointers[0].image.data.attributes.url" :title="item.pointers[0].text" />
          <ContentBoxVue :srcImg="item.pointers[1].image.data.attributes.url" :title="item.pointers[1].text" />
        </div>
      </div>

      <img class="imgCal" :src="data[0]?.section_image.media.data.attributes.url" />

      <div class="textGrid">
        <div v-for="item in data" :key="item.id">
          <ContentBoxVue :srcImg="item.pointers[2].image.data.attributes.url" :title="item.pointers[2].text" />
          <ContentBoxVue :srcImg="item.pointers[3].image.data.attributes.url" :title="item.pointers[3].text" />
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
    data: {
      type: Array,
       required: true,
    }
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
  align-items: center;
}
</style>