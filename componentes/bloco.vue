<script setup>
const props = defineProps({
  imagemSrc: String,
  mensagem: String,
  abreviacao: String,
  nivel : String,
})

const { imagemSrc, mensagem, abreviacao, nivel } = props;
</script>

<template class="tudo">
  <div class="pai">
    <img class="img" :src="imagemSrc"/>
    <div class="titulo"><b>{{ mensagem }}</b></div>
    <div class="abreviação">{{ abreviacao }}</div>
    <div class="nível">{{ nivel }}</div>
    <img class="ft" src="~/assets/Edit.jpg">
  </div>
</template>

<script>
export default {
  name: 'bloco',
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,400;1,500&display=swap');
.tudo{
  box-sizing: border-box;
  position:absolute;
}
.pai{
  width: 487px;
  height: 239px;
  flex-shrink: 0;
  border-radius: 8px;
  border: 1.5px solid #B2D2B7;
  background: #FFF;
}
.img{
  width: 487px;
  height: 120px;
  flex-shrink: 0;
}
.titulo{
  position: relative;
  margin-left: 20px;
  font-family: Poppins;
  font-size: 18.884px;
  font-weight: bold;
  font-style: normal;
  font-weight: 900;
  line-height: bold;
  margin-top: 12px;
}
.abreviação{
  position: relative;
  margin-left: 20px;
  font-family: Poppins;
  font-size: 15.107px;
  font-style: normal;
  font-weight: 600;
  line-height: normal;
  color: #7C9C81;
}
.nível{
  position: relative;
  margin-left: 20px;
  font-family: Poppins;
  font-size: 15.107px;
  font-style: normal;
  font-weight: 600;
  line-height: normal;
  color: #7C9C81;

}
.img{
  border-radius: 8px 8px 0px 0px;
}
.ft{
  position: absolute;
  margin-left: 450px;
  margin-top: -70px;
}
</style>