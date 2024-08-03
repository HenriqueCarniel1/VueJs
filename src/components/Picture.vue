<template>
  <img :src="avatar" :alt="descricao" />
</template>
  
  <script>
export default {
  name: "Picture",
  data() {
    return {
      avatar: require("../assets/avatar.png"),
      descricao: "Matheus Battisti",
    };
  },
};
</script>
  