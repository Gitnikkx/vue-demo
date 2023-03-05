<template>
  <div class="headerDiv">
    <header>
      <div>
        <img src="../public/assets/logo-500.png" alt="logo" />
      </div>
      <div class="subMenu" v-for="item in list" :key="item.id">
        <a class="a" :href="item.link" target="_blank">
          <p>{{ item.text }}</p></a
        >
      </div>

      <div class="button">
        <a class="a" href="http://www.google.com" target="_blank">
          <p class="p">{{ titleBtn }}</p>
        </a>
      </div>
    </header>
  </div>
</template>
  
  <script>
export default {
  name: "HeaderC",
  props: {
    titleBtn: { type: String, default: "Button Title" },
    list: {
      type: Array,
      default: () => [
        {
          id: 0,
          text: "Calcium Calculator",
          link: "https://stackoverflow.com/",
        },
        { id: 1, text: "What’s New", link: "https://google.com" },
        { id: 2, text: "Blogs", link: "https://twitter.com" },
        { id: 3, text: "FAQ", link: "https://stackoverflow.com" },
        { id: 4, text: "Contact Us", link: "https://facebook.com" },
      ],
    },
  },
};
</script>
  
<style>
.headerDiv{
  display: flex;
  justify-content: center;
  width: 100%;
  z-index: 88;
}

header {
  display: flex;
  align-items: center;
  width: 92%;
  height: 78px;
  background-color: white;
  position: fixed;
  top: 0;
  border-radius: 0px 0px 8px 8px;
  padding: 16px;
  padding-top: 5px;
  padding-bottom: 5px;
  z-index: 88;
}

.subMenu {
  display: flex;
  margin-left: 60px;
  gap: 32px;
  cursor: pointer;
}

.button {
  display: flex;
  width: 216px;
  height: 45px;
  background: #121d64;
  border-radius: 4px;
  position: absolute;
  justify-content: center;
  align-items: center;
  color: white;
  right: 16px;
  cursor: pointer;
}
.a {
  text-decoration: none;
} 
.p {
  color: white;
  size: 24px;
}
</style>
  