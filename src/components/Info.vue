<template>
  <p v-if="esta_trabalhando">Estou trabalhando no momento.</p>
  <p>Estou em busca de novas oportunidades!</p>
  <p>Utilizo as seguintes tecnologias:</p>
  <ul>
    <li>JavaScript</li>
    <li>PHP</li>
    <li>Python</li>
  </ul>
  <p>Mande uma mensagem para: matheus@email.com</p>
</template>
  <script>
export default {
  name: "Info",
  data() {
    return {
      esta_trabalhando: false,
    };
  },
};
</script>