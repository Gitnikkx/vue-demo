<template>
  <div>
    <Header titleBtn="BUY NOW" />
    <div class="hero_section">
      <img
        class="banner_img"
        src="../public/assets/hero_banner.jpg"
        alt="banner"
        width="100%"
      />
    </div>

    <div class="pill_section">
      <img src="../public/assets/pill.png" alt="pill" />
      <h2>
        Of Indian women have Vitamin D and Calcium deficiency, leading to a
        higher risk of osteoporosis
      </h2>
    </div>

    <CalciumSection />
    <CalciumNeeds />
    <DiscoverLivingSection />
    <FAQVue/>
  </div>
</template>

<script>
import Header from "../components/Header.vue";
import CalciumSection from "../components/CalciumSection.vue";
import CalciumNeeds from "../components/CalciumNeeds.vue";
import DiscoverLivingSection from "../components/DiscoverLivingSection.vue";
import FAQVue from '../components/FAQ.vue';

export default {
  name: "App",
  components: {
    Header,
    CalciumSection,
    CalciumNeeds,
    DiscoverLivingSection,
    FAQVue,
  },
  data() {
    return {
      title: "My Blog",
      data: [],
      pillData: {},
    };
  },
  async fetch() {
    const response = await fetch(
      "https://torrent-pharma-api.letschbang.com/api/pages/bySlug/home-page"
    );
    const posts = await response.json();
    const data = posts?.data[0]?.attributes?.banner;
    const pillData = posts?.data[0]?.attributes?.sectionTwo[0];
    //console.log(pillData?.sub_text);
  },
};
</script>

<style>
.hero_section {
  max-width: 1440px;
}

.banner_img img {
  height: auto;
  max-width: 100vw;
  object-fit: contain;
}

.pill_section {
  margin-top: 50px;
  background: rgba(206, 232, 243, 0);
  display: grid;
  place-items: center;
}
</style>
