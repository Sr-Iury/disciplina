<template>
  <div class="container">
    <div>
      <input class="campo" id="searchbar" type="text" name="searchbar()" placeholder="Procure uma disciplina" onkeyup="search()">
    <img src="~/assets/search.jpg" alt="" />
    
    </div>


    <div class="disciplinas">
      <div class="disciplina">
        <img class="ft" src="~/assets/Foto.png" alt="" />
        <h1 class="nome">Linguagem e Lógica de Programação</h1>
        <p class="abr">Abreviação: L. L. Prog.</p>
        <p class="niv">Nível: Técnico Integrado</p>
        <img class="lapis" src="~/assets/Edit.jpg" alt="" />
      </div>

      <div class="disciplina">
        <img class="ft" src="~/assets/Foto.png" alt="" />
        <h1 class="nome">Linguagem e Lógica de Programação</h1>
        <p class="abr">Abreviação: L. L. Prog.</p>
        <p class="niv">Nível: Técnico Integrado</p>
        <img class="lapis" src="~/assets/Edit.jpg" alt="" />
      </div>
    </div>
  </div>
</template>

<style>
.container{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
.campo{
  border-radius: 14px;
  border: 1.5px solid #B2D2B7;
  width: 490px;
  height: 55.046px;
}
.disciplina {
  border-radius: 8px;
  border: 1.5px solid #B2D2B7;
  background: #FFF;
  width: 487px;
  height: 239px;
  flex-shrink: 0;
  position: absolute;
  margin-left: 250px;
}
.ft{
  position: relative;
  display: flex;
  width: 487px;
  height: 120px;
  justify-content: center;
  align-items: center;
  flex-shrink: 0;
  border-radius: 8px 8px 0px 0px;
}
.nome{
  position: relative;
  font-family: Poppins;
  font-size: 18.884px;
  font-style: normal;
  font-weight: 700;
  line-height: normal;
  color: black;
}
.abr{
  position: relative;
  font-family: Poppins;
  font-size: 15.107px;
  font-style: normal;
  font-weight: 600;
  line-height: normal;
  color: #7C9C81;
}
.niv{
  position: relative;
  font-family: Poppins;
  font-size: 15.107px;
  font-style: normal;
  font-weight: 600;
  line-height: normal;
  color: #7C9C81;
}
.lapis{
  position: relative;
  margin-left: 432px;
}
</style>

<script>
function search(){
  let input = document.getElementById("searchbar").value;
  input = input.toLowerCase();
  let x = document.getElementsByClassName("disciplina");
  for(i = 0; i < x.length; i++)
  {
    if(!x[i].innerHTML.toLowerCase().includes(input)){
      x[i].computedStyleMap.display = "none";
    }
    else{
      x[i].style.display = "list-item"
    }
  }
}
</script>