<template>
  <div class="continerBox">
    <div class="imgBox">
      <img src="../public/assets/slider-img.png" width="400px" height="230px" />
    </div>
    <div style="margin-top: 24px">Calcium 101</div>
    <div style="margin-top: 8px">
      <p class="sliderHeading">The Story of Your Bones: Calcium at Every Age</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "SliderBox",
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
