<template>
    <div>

        <h3>Contador con condicional</h3>

        <h3>{{ valor }}</h3>

        <button @click="sumar">+</button> 
        <br>
        <br>
        <div v-if="valor > 10">
            <h3>El valor es mayor a 10</h3>
            <button @click="restar">-</button>
        </div>


    
    </div>

</template>

<script setup>

    import { ref } from 'vue'

    const valor = ref(0)

    function sumar() {valor.value++}

    function restar() {valor.value--}

</script>

<style scoped>

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

    div {
        background-color: #f2f2f2;
        padding: 20px;
        border-radius: 12px;
        box-shadow: 0 12px 16px 0 rgba(0,0,0,0.24), 0 17px 50px 0 rgba(0,0,0,0.19);
    }


</style>
