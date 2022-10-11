<template>
  
   <div class="container">
    <div class="p-3 m-5">
  <h1>Hola desde VUE.js 3</h1>
  <h2>V-html</h2>
  <br>
  <span class="text-primary" v-html= "holis"></span><br>
  </div>
  <hr>
  <div class="p-3">

    <h1>V-show</h1>
    <h3>Tu edad es: {{edad}}</h3>
    <h2 v-if="edad >=18 && edad >0 && edad<100">Mayor de edad</h2>
    <h2 v-else-if="edad<18 && edad > 0 && edad <100">Menor de edad</h2>
    <h2 v-else>Edad Invalida</h2>
    <button class="btn btn-primary m-1" @click="inc()">Incrementar</button>
    <button class="btn btn-danger m-1" @click="dis()">Disminuir</button>
    <hr>
    <h1>V-for</h1>
    <ul>
      <li>{{usuarios[0]}}</li>
      <li>{{usuarios[1]}}</li>
      <li>{{usuarios[2]}}</li>
      <li>{{usuarios[3]}}</li>
      <li>{{usuarios[4]}}</li>
    </ul>

    <ul>
      <li v-for="usuario in usuarios" class="text">{{ usuario }}</li>
    </ul>
    <br>
<ul>
  <li v-for ="(usuario, index) in usuarios">{{ index }}: {{ usuario }}</li>
</ul>
<br>
<ul>
  <li v-for ="(usuario, index) in usuarios" :key="index">{{ index }}: {{ usuario }}</li>
</ul>
<br>
<ul>
  <li v-for ="(valor, clave) in uusuarios" :key="clave">{{ clave }}: {{ valor }}</li>
</ul>
<hr />
<h1>v-bind</h1>
<img v-bind:src="url" alt="No hay internet">
 
<hr />
</div>
 
<h1 class="text-left">v-on</h1>
<div class="p-5 m-5" id="dbclic"  @dblclick="click">
<div class="contador"> 
  <br>
  <span class="estilo">{{ clicks }}</span>
  </div>
</div>

   </div>

</template>
  
  <script>
    export default{
      data: () => ({
        titulo: "Hola desde VUE.js",
        holis: "<h3> Soy un H3 </h3>",
        edad:0,
        usuarios :["Evelin", "Itzel", "Alan","Carlos", "Betty"],
        clicks: 0,
        url: "https://cdn.svgporn.com/logos/descript-icon.svg"
      }),
      methods:{
      inc(){
        this.edad++;
      },
      dis(){
        this.edad--;
      },
      click() {
      this.clicks++;
    }

    }
    };
  </script>
  
  <style scoped>
  div{
    text-align: center;
    margin: 0px 2rem;
  }
  ul,li{
    line-height: 16px;
    list-style:inside;
    text-align:center;
  }
  .bg-dma{
    background-color: rgb(255, 228, 232);
  }
  .estilo{
    font-weight: 600;
    color:purple;
    font-size: 20px;
  }
  img{
    width: 170px;
  }
  h1{
    color: blueviolet;
  }
  #dbclic{
    background-color: rgb(255, 169, 169);
    border-radius: 10px;
  }
  </style>