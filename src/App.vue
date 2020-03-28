<template>
  <div id="app">
    <Main />
  </div>
</template>

<script>
import Main from './components/main.vue'

export default {
  name: 'App',
  components: {
    Main
  }
}
</script>

<style>
#app {
  font-family: 'Open Sans', sans-serif; 
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  height:100%;
}

body,html {
  width:100%;
  height:100%;
  margin:0;
}
</style>
