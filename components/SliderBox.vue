<template>
  <div class="continerBox">
    <div class="imgBox">
      <img v-bind:src="imgSrc" width="400px" height="230px" />
    </div>
    <div style="margin-top: 24px">{{ tag }}</div>
    <div style="margin-top: 8px">
      <p class="sliderHeading">{{ heading }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "SliderBox",
  props: {
    tag: {
      type: String,
    },
    heading: {
      type: String,
    },
    imgSrc: {
      type: String,
    },
  },
};
</script>

<style scoped>
.continerBox {
  width: 400px;
  height: auto;
  margin-right: 15px;
}
.imgBox {
  width: 500px;
  height: 230px;
}
.sliderHeading {
  color: #121d64;
  font-size: 14px;
  line-height: 17.5px;
  font-weight: 400;
  max-width: 450px;
}
</style>
