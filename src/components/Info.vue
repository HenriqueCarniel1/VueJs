<template>
  <p v-if="esta_trabalhando">Estou trabalhando no momento.</p>
  <p v-else>Estou em busca de novas oportunidades!</p>
  <p>Utilizo as seguintes tecnologias para backend:</p>
  <ul>
    <li v-for="(tecnology, index) in backend_tecnolagies" :key="index">
      {{ tecnology }}
    </li>
  </ul>
  <p>Utilizo as seguintes tecnologias para o frontend:</p>
  <ul>
    <li v-for="tecnology in frontend_tecnolagies" :key="tecnology.id">
      {{ tecnology.tecnology }}
    </li>
  </ul>
  <div>
    <button @click="showEmail">{{ texto_botao }}</button>
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
      texto_botao: "Mostrar e-mail",
      backend_tecnolagies: ["Javascript", "PHP", "NodeJS", "Java", "C#"],
      frontend_tecnolagies: [
        { id: 1, tecnology: "HTML" },
        { id: 2, tecnology: "CSS" },
        { id: 3, tecnology: "Javascript" },
        { id: 4, tecnology: "Vue" },
      ],
    };
  },

  methods: {
    showEmail() {
      this.mostrar_email = !this.mostrar_email;

      if (!this.mostrar_email) {
        this.texto_botao = "Mostrar e-mail";
      } else {
        this.texto_botao = "Esconder e-mail";
      }
    },
  },
};
</script>