<template>
<div>
    
    <h1>Actividad 1: Contador +-</h1>
    
    <h3>{{ res }}</h3>

<button @click="sumar">+</button>
<br>

<button @click="restar">-</button>

<br>
<br>

</div>
</template>

<script setup>
import { ref } from 'vue'

const res = ref(0)

function sumar() {
    res.value++
}

function restar() {
    res.value--
}


</script>

<style scoped>
/**
  aplicar hermosos estilos y colores este componente que quede bonito
 **/

h1 {
    color: blue;
}

h3 {
    color: green;
}

button {
    background-color: #4CAF50;
    border: none;
    color: white;
    padding: 15px 32px;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 16px;
    margin: 4px 2px;
    cursor: pointer;
    border-radius: 12px;
    box-shadow: 0 12px 16px 0 rgba(0,0,0,0.24), 0 17px 50px 0 rgba(0,0,0,0.19);
}

button:hover {
    background-color: #45a049;
    box-shadow: 0 0 0 0 rgba(0,0,0,0.24), 0 0 0 0 rgba(0,0,0,0.19);
    transition: all 0.2s ease;
}



</style>
