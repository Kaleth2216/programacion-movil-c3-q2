# Manual de Componentes y Vistas - Proyecto Citas Médicas

## Componente CRUD - CitaAccionesCrud
Este componente agrupa las acciones de creación, lectura, actualización y eliminación (CRUD) en un solo lugar. Es útil para realizar operaciones de gestión sobre las citas.

### Código del Componente

```vue
<template>
  <div>
    <ion-button color="primary">Crear</ion-button>
    <ion-button color="secondary">Leer</ion-button>
    <ion-button color="tertiary">Actualizar</ion-button>
    <ion-button color="danger">Eliminar</ion-button>
  </div>
</template>

<script>
export default {
  name: 'CitaAccionesCrud',
};
</script>

<style scoped>
/* Estilos específicos para el componente */
</style>
```
Uso del Componente en una Vista
Este componente se utiliza en la vista de Inicio.vue para permitir a los usuarios gestionar las citas de manera directa desde la página de inicio.

Vista de Inicio
La vista Inicio.vue actúa como la página principal del proyecto de citas médicas. En esta vista se presenta un mensaje de bienvenida y el componente CitaAccionesCrud para gestionar citas.
```vue
<!-- Vista de Inicio -->
<template>
  <ion-content>
    <CitaAccionesCrud></CitaAccionesCrud>
  </ion-content>
</template>

<script>
import CitaAccionesCrud from '../components/CitaAccionesCrud.vue';

export default {
  name: 'Inicio',
  components: {
    CitaAccionesCrud,
  },
};
</script>

<style scoped>
/* Estilos específicos para la vista */
</style>
```

## Componente de Formulario - CitaFormulario
Este componente CitaFormulario permite al usuario ingresar los detalles de una nueva cita, incluyendo la selección de fecha, hora y otros datos relevantes.

```html
<!-- Componente CitaFormulario -->
<template>
  <div>
    <cita-campo-entrada label="Nombre del Paciente"></cita-campo-entrada>
    <cita-selector-fecha></cita-selector-fecha>
    <cita-selector-hora></cita-selector-hora>
    <cita-boton-confirmar></cita-boton-confirmar>
  </div>
</template>

<script>
import CitaCampoEntrada from './cita-campo-entrada.vue';
import CitaSelectorFecha from './cita-selector-fecha.vue';
import CitaSelectorHora from './cita-selector-hora.vue';
import CitaBotonConfirmar from './cita-boton-confirmar.vue';

export default {
  name: 'CitaFormulario',
  components: {
    CitaCampoEntrada,
    CitaSelectorFecha,
    CitaSelectorHora,
    CitaBotonConfirmar,
  },
};
</script>

<style scoped>
/* Estilos específicos para el componente */
</style>
```

## Evidencia
![Captura de pantalla de la evidencia](file:///C:/Users/KALETH/Downloads/md.png)


