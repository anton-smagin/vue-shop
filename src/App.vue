<template>
  <div id="app">
    <h1>Geek Shop</h1>
    <Shop/>
  </div>
</template>

<script>
import Shop from './components/Shop.vue'

export default {
  name: 'app',
  components: {
    Shop
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
