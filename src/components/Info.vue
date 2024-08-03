<template>
  <p v-if="esta_trabalhando">Estou trabalhando no momento.</p>
  <p v-else>Estou em busca de novas oportunidades!</p>
  <p>Utilizo as seguintes tecnologias:</p>
  <ul>
    <li>JavaScript</li>
    <li>PHP</li>
    <li>Python</li>
  </ul>
  <div>
    <button @click="showEmail">Mostrar e-mail</button>
    <p v-show="mostrar_email">mande um email para: {{ email }}</p>
  </div>
  <p>Mande uma mensagem para: matheus@email.com</p>
  <p>
    para acessar meu portfolio
    <a v-bind:href="meu_link" target="_blank">Basta clicar aqui</a>
  </p>
  <Picture />
</template>
  <script>
import Picture from "./Picture.vue";

export default {
  name: "Info",

  components: {
    Picture,
  },

  data() {
    return {
      esta_trabalhando: false,
      mostrar_email: false,
      email: "teste@gmail.com",
      meu_link: "https://google.com",
    };
  },

  methods: {
    showEmail() {
      this.mostrar_email = !this.mostrar_email
    }
  }
};
</script>