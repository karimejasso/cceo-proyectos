<script setup>
const name = "vue dinamico" ;
const styleColor = "color:blue";
const arrayColores = ["ble","red","morado"];
const activo = false;
const arrayFrutas =["manzana","pera","uva"];
</script>

<template>
  <h1>holaaaaaaaaa {{ name.toUpperCase() }}</h1>
  <h2 :style="styleColor">soy azul</h2>
  <h3>
    {{ activo ? "estoy activo" : "estoy inactivo" }}
  </h3>
  <h2 v-if = "activo"> estoy activo</h2>
  <p v-else>estoy inactivo</p>
  <ul>
    <li v-for = "(fruta, index) in arrayFrutas" :key="index">
      {{ index }} - {{ fruta }}
    </li>
  </ul>
  
</template>

<style>
h1 {
    color: aqua;
}
</style>
