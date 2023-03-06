<template>
  <div style="margin: 80px">
    <h1>Frequently Asked Questions</h1>
    <div class="faqcontainer">
      <div
        class="flexButtons"
        style="width: fit-content"
        v-for="item in [0, 1, 2, 3, 4]"
        :key="item"
      >
        <p class="flex-p">Calcium 101</p>
      </div>
    </div>

    <!-- <div>
      <div style="display: flex; justify-content: space-between">
        <div @click="toggleAnswer" style="cursor: pointer">
          <p class="p-text">Why should one take Shelcal</p>
        </div>
        <div style="width: fit-content" @click="toggleCross">
          <img src="../public/assets/plus.png" width="64px" height="40px" />
        </div>
      </div>
      <div v-show="showAnswer">
        <p class="p-ans">
          The first step is to complete a comprehensive assessment that will
          seek to understand your current sleep quality and some of the other
          lifestyle and healthcare factors that might be relevant. From there,
          Deep will recommend a care path that will include either a behavioral
          program or a telemedicine visit with a sleep specialist. You will
          always have the option to select which care path you would prefer.
        </p>
      </div>
    </div> -->
    <div v-for="item in list" :key="item.id">
      <FAQDiv :question="item.question" :answer="item.answer" />
    </div>
  </div>
</template>

<script>
import FAQDiv from "./FAQDiv.vue";
export default {
  name: "FAQSection",
  components: {
    FAQDiv,
  },
  props: {
    list: {
      type: Array,
      default: () => [
        {
          id: 0,
          question: " 1.) Why should one take Shelcal",
          answer:
            "The first step is to complete a comprehensive assessment that will seek to understand your current sleep quality and some of the other lifestyle and healthcare factors that might be relevant.From there, Deep will recommend a care path that will include either a behavioral program or a telemedicine visit with a sleep specialist. You will always have the option to select which care path you would prefer.",
        },
        {
          id: 1,
          question: " 2.) What is the recommended Shelcal 500 dosage?",
          answer:
            "The second step is to complete a comprehensive assessment that will seek to understand your current sleep quality and some of the other lifestyle and healthcare factors that might be relevant.From there, Deep will recommend a care path that will include either a behavioral program or a telemedicine visit with a sleep specialist. You will always have the option to select which care path you would prefer.",
        },
        {
          id: 2,
          question: " 3.) What are some uses of Shelcal 500 tablets?",
          answer:
            "The third step is to sleep or visit with a sleep specialist. You will always have the option to select which care path you would prefer.",
        },
        {
          id: 3,
          question: " 4.) Why should one take Shelcal",
          answer:
            "seek to understand your lifestyle and healthcare factors that might be relevant.From there, Deep will recommend a care path that will include either a behavioral program or a telemedicine visit with a sleep specialist. You will always have the option to select which care path you would prefer.",
        },
      ],
    },
  },
  data() {
    return {
      showAnswer: false,
      showCross: true,
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
.faqcontainer {
  display: flex;
  gap: 10px;
}

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
</style>
