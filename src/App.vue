<template>
  <div>
    <div class="p-3 bg-light m-5">
    <h1>Universidad Tecnologica de Tehuacán</h1>
    <h2>Aplicaciones Orientadas a Servicios</h2>
    <h3>Grupo 4B</h3>
    <h1>Directivas en VUE.js</h1>
  </div>
    <hr />
  <h2>V-text</h2>
  <span class="text-primary" v-text= "'Hola desde la directiva v-text'"></span>
  <br>
  <span>Hola desde la directiva v-text</span>
  <br>
  <span class="text-primary" v-text= "titulo"></span>
  <br>
  <span class="text-success">Esta es una trasmutacion de texto {{titulo}}, con una variable prop </span>
  <br>
  <span class="text-primary" v-text= "titulo"></span>
  <br><br>
  
  </div>
  </template>
  
  <script>
    export default{
      data: () => ({
        titulo: "Hola desde VUE.js",
      }),
    };
  </script>
  
  <style scoped>
  div{
    text-align: center;
    margin: 0px 2rem;
  }
  </style>