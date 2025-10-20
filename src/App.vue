<script>
import Buscador from './components/Buscador.vue';
import Listado from './components/Listado.vue';
export default {
  name: 'App',
  components: { Buscador, Listado }
}
</script>

<template>
  <header>
  </header>

  <main>
    <Buscador />
    <Listado />
  </main>

  <footer>
  </footer>
</template>

<style scoped>

main {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

</style>
