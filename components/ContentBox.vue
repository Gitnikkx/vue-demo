<template>
  <div class="container">
    <img class="boxImg" v-bind:src="srcImg" />
    <p class="boxText">{{ title }}</p>
  </div>
</template>

<script>
export default {
  name: "Box",
  props: {
    title: { type: String, default: "Button Title" },
    srcImg: { type: String },
  },
};
</script>

<style scoped>
.container {
  max-width: 315px;
  height: auto;
  display: flex;
  align-items: center;
  gap: 24px;
}
.boxImg {
  width: 80px;
  height: 80px;
  object-fit: contain;
}
.boxText {
  font-size: 21px;
  font-weight: 700;
  color: #121d64;
  max-width: 210px;
  text-align: left;
  line-height: 29px;
}
</style>