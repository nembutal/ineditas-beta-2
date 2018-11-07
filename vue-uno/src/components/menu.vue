<template lang="html">
  <nav class="menu" id="menu">
    <div class="barra-responsive">
      <a v-on:click="menua" id="btnabrir">A</a>
      <a v-on:click="menuc" id="btncerrar">X</a>
    </div>
    <div class="menu-contenedor" id="menu-contenedor">
      <a href="#" >btn1</a>
      <a href="#">btn2</a>
      <a href="#">btn3</a>
      <a href="#">btn4</a>
    </div>
  </nav>
</template>
/*----------*/
<script>
export default {
  mounted(){
    var menu = document.getElementById('menu');
    var alto = menu.offsetTop;

    window.addEventListener('scroll', function(){
      if(window.pageYOffset > alto){
        menu.classList.add('fixed');
      }else{
        menu.classList.remove('fixed');
      }
    }),
    window.onresize = function(){
      var cerrarmenu = document.getElementById('btncerrar');
      var abrirmenu = document.getElementById('btnabrir');
      var ancho = window.innerWidth;
      var menuresp = document.getElementById('menu-contenedor');
      if(ancho < 800){
        menuresp.style.transition = "max-height 0.2s";
        menuresp.style.maxHeight = "0px";
        abrirmenu.style.display = "block";
        cerrarmenu.style.display = "none";
      }else{
        menuresp.style.transition = "max-height 0.8s";
        menuresp.style.maxHeight = "800px";
      }
    }
  },
  methods:{
        menua: function(){
      var cerrarmenu = document.getElementById('btncerrar');
      var abrirmenu = document.getElementById('btnabrir');
      var menuresp = document.getElementById('menu-contenedor');
      menuresp.style.transition = "max-height 0.8s";
      menuresp.style.maxHeight = "800px";
      abrirmenu.style.display = "none";
      cerrarmenu.style.display = "block";
    },
        menuc:function(){
      var cerrarmenu = document.getElementById('btncerrar');
      var abrirmenu = document.getElementById('btnabrir');
      var menuresp = document.getElementById('menu-contenedor');
      menuresp.style.transition = "max-height 0.2s";
      menuresp.style.maxHeight = "0px";
      abrirmenu.style.display = "block";
      cerrarmenu.style.display = "none";
    },
  }


}
</script>

/*----------*/


<style lang="css">
.menu{
  width:100%;
  background:black;
  display: flex;
  justify-content: center;
  transition: all 1s;
  position:relative;
}
.menu-contenedor{
  width:100%;
  max-width:1400px;

  display:flex;
  justify-content: flex-end;
}
.menu-contenedor a{
  padding:10px;

  color:white;
  text-decoration:none;
}
.menu-contenedor a:hover{
  background:gray;
}
.fixed{
  position:fixed;
  top:0px;
  left:0px;
}
.barra-responsive{
  width:100%;
  background:black;
  justify-content:flex-start;
  display:none;
}
.barra-responsive a{
  padding:10px;
  background:black;
  text-decoration:none;
  color:white;
  cursor:pointer;
}
@media screen and (max-width:800px){
  .barra-responsive{
    display:flex;
  }
  .menu-contenedor{
    display:flex;
    position:absolute;
    top:100%;
    flex-flow:column;
    background:black;
    max-height:0px;
    overflow:hidden;
  }
  #btncerrar{
    display:none;
  }
}
</style>
