<!-- components/Saludo.vue -->
<template>
  <div>
    <h1>{{ mensaje }}</h1>
    <button @click="cambiarMensaje">Cambiar Mensaje</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      mensaje: '¡Hola Vue!'
    }
  },
  methods: {
    cambiarMensaje() {
      this.mensaje = '¡Mensaje cambiado!'
    }
  }
}
</script>

<style scoped>
h1 {
  color: red;
}
</style>

