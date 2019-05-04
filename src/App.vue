<template>
  <div id="app">
    <RadioButton/>
  </div>
</template>

<script>
import RadioButton from './components/RadioButton.vue'

export default {
  name: 'app',
  components: {
    RadioButton
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
