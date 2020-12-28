<template>
  <div id="app">
    <pm-Box />
  </div>
</template>

<script>
import pmBox from './components/pmBox.vue'

export default {
  name: 'App',
  components: {
    pmBox
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
