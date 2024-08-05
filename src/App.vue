<template>
  <div class="menu">
    <a v-for="navMenu in menu" :key="navMenu">{{ navMenu }}</a>
  </div>
  <div>
    <img src="./assets/logo.png" alt="Vue logo" />
  </div>
  <!-- product: 배열의 각 개별 항목
       products: 첫 번째 항목부터 마지막 항목까지 차례로 `product` 변수에 담김
       index: 0부터 시작해서 배열의 마지막 항목까지 순서대로 증가
   -->
  <div v-for="(product, index) in products" :key="index">
    <h2>{{ product }}</h2>
    <!-- 1. 50 + (0 * 10) 
         2. 50 + (1 * 10)
         3. 50 + (2 * 10) -->
    <p>{{ price + (index * 10) }}만원</p>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      menu: ["Home", "Shop", "About"],
      products: ["광장시장", "한민시장", "구경시장"],
      price: 50,
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
