<script setup>
defineEmits(['hmpg', 'carrinho'])
</script>

<template>
  <header>

      <h1><a href="./App.vue"><img src="/public/img/logo.png" alt="GAMES LFR"></a></h1>

      <div class="pesquisar">
        <input type="text" placeholder="Pesquisar" >
        <span class="fa-solid fa-magnifying-glass"></span>


      </div>
      <div style="display: flex; align-items: center;">
      <ul class="ulPrincipal">
        <li  @click="$emit('hmpg')">
          <a>
            HomePage
          </a>
        </li>

        <li >
          <a href="">
            Termos
          </a>
        </li>

        <li>
          <a href="">
            Equipe
          </a>
        </li>

        <li>
          <a href="">
            Devoluções
          </a>
        </li>


      </ul>
      <ul class="icon">
        <li @click="$emit('carrinho')">
          <a ><span class="fa-solid fa-cart-shopping"></span></a>
        </li>

        <li >
          <a href=""><span class="fa-solid fa-heart"></span></a>
        </li>

        <li >
          <a href=""><span class="fa-solid fa-user"></span></a>
        </li>
      </ul>
    </div>

    </header>
</template>

<style scoped>
header{
  display: flex;
  padding: 2vw 2vw;
  justify-content: space-between;
  align-items: center;
  background: linear-gradient(135deg, #171a21, #1b2838, #2a475e);
  font-family: 'comfortaa';
  box-shadow: 0 0 20px rgba(102, 192, 244, 0.1);
  color: #c7d5e0;
  border-bottom: 1px solid rgba(255, 255, 255, 0.1);
}

header h1 img{
  width: 5vw;
  height: 5vw;
  border-radius: 2vw;
  box-shadow: 0 0 10px rgba(255, 255, 255, 0.1);
}

header input{
    font-size: 0.6rem;
     border: 2px solid #66c0f4;
    border-radius: 10vw;
    padding: 1vw;
    font-family: 'comfortaa';
}

header input:hover{
  background-color: rgba(226, 234, 238, 0.856);
  transition: 0.3s;
}

header ul{
  display: flex;
  align-items: center;
}
header ul.ulPrincipal li{
  margin: 0 2vw;
  font-size: 0.6rem;
  padding: 0.5vw 1vw;
  cursor: pointer;
  border-radius: 2vw;
  width: 15%;
  text-align: center;
  color: #c7d5e0;
}
header ul.ulPrincipal li a {
  color: aliceblue;
}

header ul.ulPrincipal li:hover{
  background-color: rgba(102, 192, 244, 0.2);
  transition: 0.3s;
}
header ul.ulPrincipal li:first-child{
  margin-left: 0;
}
header ul.ulPrincipal li:last-child{
    margin-right: 5vw;
}
header ul.icon li:nth-child(2){
    margin: 2vw ;
}
header ul.icon li{
    font-size: 0.8rem;
    padding:0.5vw 1vw ;
    border-radius: 2vw;
    cursor: pointer;
    color: #c7d5e0
}
header ul.icon li span {
  color: aliceblue;
}

header ul.icon li:hover{
  background-color: rgba(102, 192, 244, 0.2);
  transition: 0.3s;
}

/*Pesquisar*/
.pesquisar {
  position: relative;
  display: inline-block;
}

.pesquisar input {
  width: 10vw;
  padding: 0.7vw;
  border: 2px solid #ccc;
  border-radius: 20vw;
  font-size: 0.6rem;
  outline: none;
}



.pesquisar span {
  position: absolute;
  top: 50%;
  right: 15px;
  transform: translateY(-50%);
  color: #aaa;
  font-size: 0.7rem;
  pointer-events: none;
}
</style>
