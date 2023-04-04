<template>
  <div id="app">
    <First msgp=" hi this is props from first"/>
    <Seconde />
  </div>
</template>

<script>

import First from './components/First.vue'
import Seconde from './components/Seconde.vue'
export default {
  name: 'App',
  components: {
    First,
    Seconde
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
