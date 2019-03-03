<template>
  <div id="start" class="container">
    <app-header></app-header>
    <app-scrums></app-scrums>
  </div>
</template>

<script>
import appHeader from './components/Header.vue'
import appScrums from './components/Scrums.vue'
export default {
  name: 'App',
  components: {
    'appHeader': appHeader,
    'appScrums': appScrums
  }
}
</script>

<style>
#start {
  margin: 20px auto;
}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
