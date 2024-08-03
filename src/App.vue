<template>
  <div>
    <primeiro-componente />
    <LifeCycle />
  </div>
</template>
<script>
// Componentes
import LifeCycle from "./components/LifeCycle.vue";
import PrimeiroComponente from "./components/PrimeiroComponente.vue";

export default {
  name: "App",
  components: {
    PrimeiroComponente,
    LifeCycle,
  },
};
</script>

<style>
  body {
    background-color: #222222;
  }
</style>