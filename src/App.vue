<template>
  <div>
    <img src="./assets/logo.png" alt="Vue logo">

    <h2>{{products[0]}}</h2>
    <p> 생선: 3만원 입니다.</p>
  </div>
  <div>
    <h2>{{products[1]}}</h2>
    <p>고기 : 2만원 입니다</p>
  </div>
  <div>
    <h2>{{products[2]}}</h2>
    <p>과일 : 4만원 입니다.</p>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      products: ['광장시장', '한민시장', '구경시장']
    }
  },
  components: {
  }
}
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
</style>
