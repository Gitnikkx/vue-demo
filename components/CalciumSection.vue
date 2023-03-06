<template>
  <div style="margin: 100px">
    <h1 style="text-align: center">{{ data[0]?.title_text }}</h1>
    <div class="calgrid">
      <div class="cardDiv">
        <img
          class="cardimg"
          :src="data[0]?.cards[0]?.image?.data?.attributes?.url"
          alt="diet"
        />
        <p class="textCal">{{ data[0]?.cards[0]?.text }}</p>
      </div>
      <img class="symbolimg" src="../public/assets/equals.svg" />
      <div class="cardDiv">
        <img
          class="cardimg"
          :src="data[0]?.cards[1]?.image?.data?.attributes?.url"
          alt="diet"
        />
        <p class="textCal">{{ data[0]?.cards[1]?.text }}</p>
      </div>
      <img class="symbolimg" src="../public/assets/equals.svg" />
      <div class="cardDiv">
        <img
          class="cardimg"
          :src="data[0]?.cards[2]?.image?.data?.attributes?.url"
          alt="1000"
        />
        <p class="textCal">
          {{ data[0]?.cards[2]?.text }}
        </p>
      </div>
    </div>
    <a
      class="a"
      href="https://torrent-pharma.letschbang.com/calculator"
      target="_blank"
    >
      <div class="testBtn">
        <p class="btnText">{{ data[0]?.cta?.cta_title }}</p>
      </div>
    </a>
  </div>
</template>

<script>
export default {
  name: "CalciumS",
  props: {
    data: {
      type: Array,
      // required: true
    },
  },
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
  gap: 50px;
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