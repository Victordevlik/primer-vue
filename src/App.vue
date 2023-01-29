<script setup>
const name= "hola vue dinamico";
 const styleColor = "color:red";
 const tipoLetra = "font-family: arial";
 const arrayColores = ["blue", "red", "white"];
 const activo = true;
</script>



<template>
  <h1>{{ name.toUpperCase() }}</h1><br>
  <h2>{{ arrayColores }}</h2>
  <h2 :style="`color: ${ arrayColores[2]} `">soy peru </h2><br>
<h2 :style="styleColor "> soy rojo</h2><br>
<h3 :style="tipoLetra "> tipo de letra</h3><br>
<!-- <h2>{{ activo? "estoy activo " : "estoy inactivo" }}</h2> -->
<h2 v-if="activo">estoy activo</h2>
<h2 v-if="!activo">estoy inactivo</h2>
<h2 v-else>estoy</h2>
</template>

<style>
h1 {
 color: green
}
</style>