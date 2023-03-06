<template>
  <div>
    <div @click="toggleAnswer" style="cursor: pointer">
      <p class="p-text">{{ question }}</p>
    </div>
    <div v-show="showAnswer">
      <p class="p-ans">
        {{ answer }}
      </p>
    </div>
  </div>
</template>



<script>
export default {
  name: "faqDiv",
  props: {
    question: {
      type: String,
    },
    answer: {
      type: String,
    },
  },
  data() {
    return {
      showAnswer: false,
    };
  },
  methods: {
    toggleAnswer() {
      this.showAnswer = !this.showAnswer;
    },
    toggleCross() {
      this.showCross = !this.showCross;
    },
  },
};
</script>


<style scoped>
.p-text {
  font-style: normal;
  font-weight: 700;
  font-size: 21px;
  line-height: 29px;
  color: #121d64;
}
.p-ans {
  font-weight: 400;
  font-size: 17px;
  line-height: 24px;
  color: #121d64;
}
</style>