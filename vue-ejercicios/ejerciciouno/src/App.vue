<template>
  <div id="app">
    <modal/>
    <cajasup/>
    <Menu/>
  </div>
</template>

<script>
import modal from './components/modal.vue'
import cajasup from './components/cajasuperior.vue'
import Menu from './components/menu.vue'

export default {
  name: 'App',
  components: {
    modal,
    cajasup,
    Menu
  }
}
</script>

<style>
*{
  padding:0px;
  margin:0px;
  box-sizing:border-box;
}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
</style>
