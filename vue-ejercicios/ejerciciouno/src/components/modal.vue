<template lang="html">
<div class="">
  <button type="button" name="button" v-on:click="abrirmodal">abrir modal</button>
<div class="backmodal" id="backmodal" v-on:click="cerrarmodal"></div>
<div class="cajamodal" id="cajamodal"></div>
</div>
</template>

<script>
export default {

  methods:{

    abrirmodal:function(){
      var back = document.getElementById('backmodal');
      var caja = document.getElementById('cajamodal');
      back.style.display = "block";
      caja.style.display = "block";
      var delay = setTimeout(function (){
        back.style.transition = "opacity 1s";
        back.style.opacity = "1";
        caja.style.transition = "opacity 1s";
        caja.style.opacity = "1";
      }, 100);
    },
    cerrarmodal:function(){
      var back = document.getElementById('backmodal');
      var caja = document.getElementById('cajamodal');
      back.style.transition = "opacity 0.8s";
      back.style.opacity = "0";
      caja.style.transition = "opacity 0.8s";
      caja.style.opacity = "0";
      var delay = setTimeout(function (){
        back.style.display = "none";
        caja.style.display = "none";
      },800);
    }
  }
}
</script>

<style lang="scss">
$color-uno:rgba(0,0,0,0.8);
$color-dos:white;
  .backmodal{
    width:100%;
    height:100vh;
    background:$color-uno;
    position:fixed;
    top:0px;
    left:0px;
    z-index:100;
    display:none;
    opacity:0;
}
.cajamodal{
  width:100%;
  max-width:800px;
  height:500px;
  background:$color-dos;
  position:fixed;
  z-index:200;
  left:0px;
  right:0px;
  bottom:0px;
  top:0px;
  margin:auto;
  display:none;
  opacity:0;
}
</style>
