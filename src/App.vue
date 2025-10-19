<script>
import Usuarios from './components/Usuarios.vue';
export default {
  name: 'APP',
  components: { Usuarios }
}
</script>

<template>
  <h1 class="title">Tabla de usuarios</h1>
  <main>
    <Usuarios />
  </main>
</template>

<style scoped>
.title {
  text-align: center;
  margin-top: 20px;
  margin-bottom: 20px;
  font-size: 40px;
  color: #2c3e50;
}
</style>
