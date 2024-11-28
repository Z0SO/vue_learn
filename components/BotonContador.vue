<template>
  <button @click="incrementar">{{ contador }}</button>
</template>

<script setup>
import { ref } from 'vue';

// Crear un contador local
const contador = ref(0);

// Función para incrementar el contador
function incrementar() {
  contador.value++;
}
</script>

