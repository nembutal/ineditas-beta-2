<template>
  <div id="app">
    <CajaDos/>
    <Menu/>
    <CajaInferior/>
    <CajaSuperior/>

  </div>
</template>

<script>
import Menu from './components/menu.vue'
import CajaSuperior from './components/cajasuperior.vue'
import CajaInferior from './components/cajainferior.vue'
import CajaDos from './components/otracaja.vue'
export default {
  name: 'App',
  components: {
    Menu,
    CajaSuperior,
    CajaInferior,
    CajaDos
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
