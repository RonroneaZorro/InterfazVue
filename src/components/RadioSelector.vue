<script>
import { ref } from 'vue';
export default {
  name: 'RadioSelector',
  setup() {
    const opcionesEstudios = [
      { value: 'universitarios', label: 'Universitarios' },
      { value: 'secundarios', label: 'Secundarios' },
      { value: 'primarios', label: 'Primarios' },
      { value: 'ninguno', label: 'Ninguno' }
    ];
    const estudiosSeleccionados = ref('universitarios');  

    return {
      opcionesEstudios,
      estudiosSeleccionados
    };
  }
};
</script>
<template>
<h1>Controles Radio y Select en Vue</h1>
<section class="radio-selector">
    <h2>Selecciona tu tipo de estudios:</h2>
    <div><label v-for="opcion in opcionesEstudios" :key="opcion.value">
        <input type="radio" v-model="estudiosSeleccionados" :value="opcion.value" :id="opcion.value">
        {{ opcion.label }}
        </label>
    </div>
    <p><strong>Estudios seleccionados:</strong> {{ estudiosSeleccionados }}</p>
</section>
</template>
<style>
.radio-selector {
  border: 1px solid #ccc;
  padding: 10px;
  border-radius: 5px;
  background-color: #f9f9f9;
  max-width: auto;
  margin: 0 auto;
  text-align: center;
  margin-top: 20px;
}
</style>