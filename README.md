# Ejecutar el proyecto

```bash
cd prueba
npm i 
npm run dev
```

---

# Guía de Aprendizaje Vue.js y Nuxt

Esta guía está diseñada para ayudarte a aprender Vue.js y Nuxt de manera estructurada, comenzando desde los conceptos básicos hasta temas más avanzados.

---

## Configuración Inicial
### Explicación
Antes de comenzar, necesitamos configurar nuestro entorno de desarrollo. Nuxt.js es un framework construido sobre Vue.js que facilita la creación de aplicaciones web universales.

#### Ejemplo de Código
```bash
# Crear nuevo proyecto Nuxt
npx create-nuxt-app mi-primer-proyecto

# Estructura básica recomendada
mi-primer-proyecto/
  ├── pages/
  ├── components/
  ├── layouts/
  ├── assets/
  └── nuxt.config.js
```

### Ejercicio
Crea un nuevo proyecto Nuxt y personaliza la configuración inicial según tus necesidades. Asegúrate de que puedas ejecutar el servidor de desarrollo.

#### Pista
Durante la configuración, selecciona JavaScript/TypeScript según tu preferencia, y elige Tailwind CSS como framework CSS para facilitar el diseño.

---

## Componentes Básicos
### Explicación
Los componentes son la base de Vue.js. Son elementos reutilizables que encapsulan lógica, estructura y estilos.

#### Ejemplo de Código
```vue
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
```

### Ejercicio
Crea un componente de tarjeta (Card) que muestre una imagen, título y descripción. Debe tener un botón que permita "dar like" y mostrar el número de likes.

#### Pista
Utiliza `data()` para manejar el estado del contador de likes y un método para incrementarlo.

---

## Composición API
### Explicación
La Composition API es una forma alternativa de organizar la lógica de los componentes, permitiendo mejor reutilización y organización del código.

#### Ejemplo de Código
```vue
<!-- components/ContadorComposition.vue -->
<template>
  <div>
    <p>Contador: {{ contador }}</p>
    <button @click="incrementar">+</button>
    <button @click="decrementar">-</button>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const contador = ref(0)

const incrementar = () => {
  contador.value++
}

const decrementar = () => {
  contador.value--
}
</script>
```

### Ejercicio
Crea un componente de lista de tareas (TodoList) utilizando la Composition API. Debe permitir agregar, eliminar y marcar tareas como completadas.

#### Pista
Utiliza `ref()` para el array de tareas y `computed()` para filtrar las tareas completadas/pendientes.

---

## Enrutamiento en Nuxt
### Explicación
Nuxt proporciona un sistema de enrutamiento basado en archivos. La estructura de archivos en el directorio `pages/` determina las rutas de tu aplicación.

#### Ejemplo de Código
```vue
<!-- pages/usuarios/[id].vue -->
<template>
  <div>
    <h1>Perfil de Usuario</h1>
    <p>ID del usuario: {{ $route.params.id }}</p>
  </div>
</template>

<script setup>
const route = useRoute()
const id = route.params.id
</script>
```

### Ejercicio
Crea una pequeña aplicación con tres páginas: inicio, lista de productos y detalle de producto. Implementa la navegación entre ellas usando tanto enlaces como navegación programática.

#### Pista
Utiliza `<NuxtLink>` para la navegación declarativa y `navigateTo()` para la navegación programática.

---

## Estado Global con Pinia
### Explicación
Pinia es la solución recomendada para el manejo de estado global en aplicaciones Vue/Nuxt modernas.

#### Ejemplo de Código
```javascript
// stores/contador.js
import { defineStore } from 'pinia'

export const useContadorStore = defineStore('contador', {
  state: () => ({
    count: 0
  }),
  actions: {
    incrementar() {
      this.count++
    },
    decrementar() {
      this.count--
    }
  },
  getters: {
    counterValue: (state) => state.count
  }
})
```

### Ejercicio
Implementa un carrito de compras usando Pinia. Debe permitir agregar/quitar productos y calcular el total.

#### Pista
Define un store con un array de productos, métodos para manipular el carrito y getters para calcular totales.

---

## Consumo de APIs
### Explicación
Nuxt proporciona utilidades para realizar peticiones HTTP de manera eficiente.

#### Ejemplo de Código
```vue
<script setup>
const { data: posts } = await useFetch('https://api.ejemplo.com/posts')
</script>

<template>
  <div>
    <article v-for="post in posts" :key="post.id">
      <h2>{{ post.title }}</h2>
      <p>{{ post.body }}</p>
    </article>
  </div>
</template>
```

### Ejercicio
Crea una página que muestre una lista de usuarios consumiendo la API de JSONPlaceholder. Implementa paginación y búsqueda.

#### Pista
Utiliza `useFetch` con parámetros de query para la paginación y búsqueda. Maneja los estados de carga y error.

---

## Middleware y Autenticación
### Explicación
Los middleware permiten ejecutar código antes de renderizar una página o grupo de páginas.

#### Ejemplo de Código
```javascript
// middleware/auth.js
export default defineNuxtRouteMiddleware((to, from) => {
  const isAuthenticated = useState('auth').value
  
  if (!isAuthenticated && to.path !== '/login') {
    return navigateTo('/login')
  }
})
```

### Ejercicio
Implementa un sistema de autenticación básico con login/logout y protección de rutas.

#### Pista
Usa `useState` para mantener el estado de autenticación y aplica el middleware a las rutas protegidas.
