<template>
  <div class="menu">
    <a v-for="navMenu in menu" :key="navMenu">{{ navMenu }}</a>
  </div>
  <div>
    <img src="./assets/logo.png" alt="Vue logo" />
  </div>
  <div v-for="(products, index) in products" :key="index">
    <h2>{{ products }}</h2>
    <p>50만원</p>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      menu: ["Home", "Shop", "About"],
      products: ["광장시장", "한민시장", "구경시장"],
    };
  },
  components: {},
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.menu {
  background: darkslateblue;
  padding: 15px;
  border-radius: 5px;
}
.menu a {
  color: white;
  padding: 10px;
}
</style>
