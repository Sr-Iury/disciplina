
<template class="t">
  <search-bar></search-bar>
  <bloco class="p1" :imagemSrc="caminhoDaImagem" :mensagem="mensagemDoPai" :abreviacao="abre" :nivel="niv" />

  <bloco  class="p2" :imagemSrc="caminhoDaImagem2" :mensagem="mensagemDoPai2" :abreviacao="abre2" :nivel="niv2" />


  <bloco class="p3" :imagemSrc="caminhoDaImagem3" :mensagem="mensagemDoPai3" :abreviacao="abre3" :nivel="niv3" />

  <adicionar/>
</template>
<script>
import bloco from '~/componentes/bloco.vue'
import adicionar from '~/componentes/adicionar.vue'
import caminhoDaImagem from '~/assets/Foto.png'
import SearchBar from "~/componentes/SearchBar.vue"
export default {
  components: {
    bloco,
    SearchBar,
    adicionar,
  },
  data() {
    return {
      caminhoDaImagem: caminhoDaImagem,
      mensagemDoPai: "Linguagem e Lógica de Programação", // Defina o valor da prop aqui
      abre: "Abreviação: L. L. Prog",
      niv: "Nível: Técnico Integrado",

      caminhoDaImagem2: "https://picsum.photos/200/300",
      mensagemDoPai2: "Matemática", // Defina o valor da prop aqui
      abre2: "Abreviação: Mat",
      niv2: "Nível: Técnico Integrado",

      caminhoDaImagem3: "https://picsum.photos/200/300",
      mensagemDoPai3: "Português", // Defina o valor da prop aqui
      abre3: "Abreviação: Port",
      niv3: "Nível: Técnico Integrado",
    };
  }
}
</script>

<style>
.t{
  box-sizing: border-box;
  position: absolute;
}
.p1
{
  position: absolute;
  margin-left: 200px;
  margin-top: 150px;
}
.p2{
  position: absolute;
  margin-top: 420px;
  margin-left: 200px;
}
.p3{
  position: absolute;
  margin-left: 720px;
  display: block; 
  margin-top: 150px;
}
</style>

