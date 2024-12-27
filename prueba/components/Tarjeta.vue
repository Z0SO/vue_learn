<!-- Crea un componente de tarjeta (Card) que muestre una imagen, título y descripción. Debe tener un botón que permita "dar like" y mostrar el número de likes. -->

<template>
    <div>
        <img src="http://placekittens.com/g/200/200" alt="Gatito">
        <h2>Titulo</h2>
        <p>Descripción</p>

        <button @click="darMeGusta">Dar Like</button>

        <button @click="quitarMeGusta">Quitar Like</button>
        <p>{{ likes }}</p>
    </div>
</template>

<!-- utilizando ref -->
<script setup>

import { ref } from 'vue'
const likes = ref(0)

const darMeGusta = () => {
    likes.value++
}
const quitarMeGusta = () => {
    likes.value--
}
    
</script>

<!--
    con data
<script>
    export default {
        data() {
            return {
                likes:0
            }
        },
        methods: {
            darLike() {
                this.likes++
            }
        }
    }
</script>
-->
