<template>
  <div class="search-bar">
    <input
    id="name"
      type="text"
      v-model="searchQuery"
      @input="handleInput"
      placeholder="Procure uma disciplina"
    />
    <img class="ft" src="~/assets/search.jpg">
  </div>
</template>

<script>
export default {
  data() {
    return {
      searchQuery: "",
    };
  },
  methods: {
    handleInput() {
      // Este método é chamado sempre que o usuário digita algo na barra de pesquisa.
      // Você pode adicionar lógica adicional aqui, se necessário.
    },
    search() {
      // Este método é chamado quando o botão "Buscar" é clicado.
      // Você pode realizar a lógica de pesquisa aqui, como fazer uma chamada à API.
      // Neste exemplo, apenas exibimos a consulta no console.
      console.log("Pesquisando por: " + this.searchQuery);
    },
  },
};
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,400;1,500&display=swap');
.search-bar {
  position: absolute;
  display: flex;
  margin-left: 200px;
  margin-top: 78px;
}

input[type="text"] {
  border-radius: 8px;
  border: 2px solid #B2D2B7;
  width: 485px;
  height: 39px;
}
::-webkit-input-placeholder{
  color: #9AB69E;
  font-family: Poppins;
  font-size: 11.287px;
  font-style: normal;
  font-weight: 600;
  line-height: normal;
  position: absolute;
  margin-left: 15px;
}
.ft{
  position: absolute;
  margin-left: 460px;
  margin-top: 12px;
  width: 14px;
  height: 18.215px;
  flex-shrink: 0;
  }
  textarea:focus, input:focus, select:focus {
    outline: 0;
}
</style>
