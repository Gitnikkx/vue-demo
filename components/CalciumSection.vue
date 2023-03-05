<template>
  <div style="margin: 100px">
    <h1 style="text-align: center">Whats your calcium quotient ?</h1>
    <div class="calgrid">
      <div class="cardDiv">
        <img class="cardimg" src="../public/assets/diet.png" alt="diet" />
        <p class="textCal">Daily Diet</p>
      </div>
      <img class="symbolimg" src="../public/assets/equals.svg" />
      <div class="cardDiv">
        <img class="cardimg" src="../public/assets/cal.png" alt="diet" />
        <p class="textCal">Calcium Suppliments</p>
      </div>
      <img class="symbolimg" src="../public/assets/equals.svg" />
      <div class="cardDiv">
        <img class="cardimg" src="../public/assets/1000.png" alt="1000" />
        <p class="textCal">
          Complete average calcium requirement for men and women
        </p>
      </div>
    </div>
    <a
      class="a"
      href="https://torrent-pharma.letschbang.com/calculator"
      target="_blank"
    >
      <div class="testBtn"><p class="btnText">TAKE THE TEST</p></div></a
    >
  </div>
</template>

<script>
export default {
  name: "CalciumS",
};
</script>

<style>
.a {
  text-decoration: none;
}
.calgrid {
  display: grid;
  grid-template-columns: auto 27px auto 27px auto;
  align-items: center;
  justify-content: center;
  gap: 10px;
}
.cardimg {
  width: 300px;
  height: 300px;
  object-fit: contain;
}
.symbolimg {
  width: 27px;
  height: 27px;
  object-fit: cover;
}
.cardDiv {
  background: cornsilk;
}
.textCal {
  font-weight: 700;
  line-height: 29px;
  size: 21px;
  color: #121d64;
  max-width: 300px;
  text-align: center;
}
.testBtn {
  background: #121d64;
  width: fit-content;
  border-radius: 4px;
  margin: auto;
  margin-top: 45px;
  cursor: pointer;
}
.btnText {
  color: white;
  font-weight: 900;
  font-size: 14px;
  line-height: 21px;
  padding: 16px 24px 16px 24px;
}
</style>