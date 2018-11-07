<template>
  <div id="app">
    <Menu/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld'
import Menu from './components/menu.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    Menu
  }
}
</script>

<style>
*{
  padding:0px;
  margin:0px;
  box-sizing: border-box;
}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
