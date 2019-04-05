<template>
  <div id="app">
    <resume></resume>
    <div id="view-options">
    </div>
  </div>
</template>

<script>
import Resume from './components/Resume.vue'


export default {
  name: 'app',
  components: {
    Resume
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
