# Nuxt Minimal Starter

Make sure to install dependencies:

```bash
# npm
npm install

```

## Development Server

Start the development server on `http://localhost:3000`:

```bash
# npm
npm run dev
```

## Production

Build the application for production:

```bash
# npm
npm run build
```

Locally preview production build:

```bash
# npm
npm run preview
```

## Cosas que se incluyen en la practica  de este proyecto

### 1. **Crear un componente de contador más complejo**
   Crea un componente que tenga dos botones:
   - Un botón para **incrementar** el contador.
   - Un botón para **decrementar** el contador.
   
   Usa `ref` para el contador y maneja las dos acciones (incrementar y decrementar).

### 2. **Condicionales y v-if en Vue**
   Crea un componente con un botón y un mensaje que se muestre solo si el contador es mayor a un valor específico. Ejemplo: "El contador ha superado el valor 5".

### 3. **Manejo de eventos y `v-model`**
   Crea un componente que permita ingresar un número en un campo de texto (input), y que al hacer clic en un botón, actualice el contador con ese número. Usa `v-model` para el campo de texto y un botón para disparar la acción.

### 4. **Componentes con Props**
   Crea dos componentes:
   - Un componente **Padre** que pase un valor como `prop` a un componente **Hijo**.
   - El componente Hijo debe mostrar el valor recibido y actualizarlo cuando el valor cambie.

### 5. **Mostrar y ocultar elementos con `v-show`**
   Crea un componente donde un botón controle la visibilidad de un mensaje. Usa `v-show` para mostrar u ocultar el mensaje al hacer clic en el botón.

### 6. **Crear un temporizador (contador de tiempo)**
   Crea un componente que simule un temporizador que cuente en segundos desde que el componente es montado. Usa `setInterval` para actualizar el contador cada segundo y muestra el tiempo transcurrido.

### 7. **Manejo de listas con `v-for`**
   Crea un componente que muestre una lista de números y un botón para agregar un nuevo número al final de la lista. Cada vez que se haga clic en el botón, un nuevo número (por ejemplo, el número de la lista + 1) debe ser agregado a la lista.

### 8. **Formulario de registro básico**
   Crea un formulario con los siguientes campos:
   - Nombre
   - Email
   - Contraseña
   
   Cuando el formulario sea enviado, valida que los campos no estén vacíos y muestra un mensaje de éxito o error.

### 9. **Transiciones entre elementos**
   Crea un componente con una lista de elementos y un botón que agregue o elimine elementos de la lista. Usa las transiciones de Vue (`<transition>`) para animar la entrada y salida de los elementos.

### 10. **Filtrar una lista**
   Crea un componente que contenga una lista de nombres y un campo de búsqueda. A medida que el usuario escribe en el campo de búsqueda, la lista debe filtrarse para mostrar solo los nombres que contienen el texto ingresado.

### 11. **Modal con `v-if`**
   Crea un componente de modal que se muestre y oculte al hacer clic en un botón. Usa `v-if` para mostrar el modal y `v-on:click` para manejar los clics fuera del modal y cerrarlo.

### 12. **Actualizar un valor mediante `v-model` en un formulario**
   Crea un formulario que tenga un `input` de texto para editar un valor. Usa `v-model` para enlazar el valor del campo con una variable en el `script` y muéstralo en otra parte del componente mientras se edita.

### 13. **Mostrar el tiempo actual en formato de 12 horas**
   Crea un componente que muestre la hora actual en formato de 12 horas (AM/PM). Puedes usar `Date` para obtener la hora y formatearla. Haz que el reloj se actualice cada segundo con `setInterval`.

### 14. **Simular una lista de productos y un carrito de compras**
   Crea una lista de productos (con nombre y precio) y un carrito de compras. Permite al usuario agregar productos al carrito y muestra el total del precio de los productos en el carrito.

### 15. **Crear un componente de "To-Do List"**
   Crea una lista de tareas pendientes (To-Do) donde puedas:
   - Agregar tareas.
   - Marcar tareas como completadas.
   - Eliminar tareas.
   
   Guarda las tareas en un array y actualiza la lista de forma dinámica.

### 16. **Manejo de temas (modo oscuro / claro)**
   Crea un botón para cambiar entre modo oscuro y modo claro. Usa clases CSS o `v-bind:class` para aplicar el tema correspondiente a la página.

### 17. **Reloj con zona horaria**
   Crea un componente que muestre la hora en diferentes zonas horarias (por ejemplo, hora en Nueva York, Londres y Tokio). Usa la API de `Intl.DateTimeFormat` o `Date` para mostrar las horas.

### 18. **Mostrar una lista de usuarios con paginación**
   Crea un componente que obtenga una lista de usuarios desde una API (puedes usar una API pública como JSONPlaceholder) y los muestre paginados. Implementa botones para avanzar y retroceder entre las páginas de usuarios.

### 19. **Ejercicio de validación de formulario**
   Crea un formulario donde el usuario deba ingresar su nombre, correo y un número de teléfono. Agrega validaciones para cada campo (como formato de correo y longitud del teléfono) y muestra un mensaje si hay errores.

### 20. **Control de visibilidad con un temporizador**
   Crea un componente que muestre un mensaje durante 5 segundos y luego lo oculte automáticamente. Usa `setTimeout` para controlar la visibilidad del mensaje.

### 21. **Cargar imágenes y mostrar un "loader"**
   Crea un componente que cargue una imagen desde una URL y muestre un "loader" (por ejemplo, un spinner) mientras la imagen se está cargando. Cuando la imagen esté lista, muestra la imagen y oculta el loader.

### 22. **Crear un contador con límite máximo**
   Crea un contador que se incremente cada vez que el usuario haga clic en un botón. Sin embargo, cuando el contador llegue a un valor máximo (por ejemplo, 10), el botón se desactivará y el contador dejará de incrementarse.

### 23. **Cargar y mostrar datos de una API externa**
   Crea un componente que haga una solicitud HTTP a una API externa (por ejemplo, obteniendo información del clima) y muestre los datos en la interfaz. Usa `fetch` o `axios` para realizar la solicitud.

### 24. **Animación con `@keyframes`**
   Crea un componente que utilice una animación CSS con `@keyframes` para animar un elemento cuando el usuario haga clic en un botón (por ejemplo, cambiar el color o el tamaño de un elemento).

### 25. **Control de estado con `provide` y `inject`**
   Crea un componente de formulario que use `provide` en el componente principal y `inject` en los componentes secundarios para compartir datos entre ellos sin tener que pasar las propiedades manualmente.

