<script>
import { ref } from 'vue';
export default {
  name: 'SelectorDia',
  setup() {
    const diasSemana = ['lunes', 'martes', 'miercoles', 'jueves', 'viernes', 'sabado', 'domingo'];
    const diaSeleccionado = ref(''); 

    return {
      diasSemana,
      diaSeleccionado
    };
  }
};
</script>
<template>
  <h1>Select de selección de única</h1>
  <div class="selector-dia">
    <h2>Selecciona un día de la semana:</h2>
    <select v-model="diaSeleccionado">
      <option disabled value="">Seleccione un día</option>
      <option v-for="dia in diasSemana" :key="dia" :value="dia">
        {{ dia.charAt(0).toUpperCase() + dia.slice(1) }} 
      </option>
    </select>

    <p><strong>Día seleccionado:</strong> {{ diaSeleccionado }}</p>
  </div>
</template>
<style> 
.selector-dia {
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