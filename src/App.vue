<script setup>
import {ref} from 'vue';

import { jogosAcao, jogosTerror, jogosSurvival, jogosMA } from './cod.js';

  

 

  const genero = ref(0);

 function action (){
  genero.value = 0
 }
 function terror (){
  genero.value = 1
 }
 function survival (){
  genero.value = 2
 }

 function MA(){
  genero.value = 3
 }



 function toggleFavorito(jogo) {
  jogo.favorito = !jogo.favorito; 
}



  const paginas = ref(0)

  function hmpg(){
    paginas.value = 0
  }
  function carrinho(){
    paginas.value = 1
  }
  function favorito(){
    paginas.value = 2
  }
  function cadastro(){
    paginas.value = 3
  }



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
      <li  @click="hmpg()">
        <a>
          HomePage
        </a>
      </li>

      <li>
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
      <li @click="carrinho()">
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
  <main>
    <div class="hmpg" v-if="paginas == 0">
  <section >
    <div>
      <h2 style="text-align: center;
      font-size: 2rem;
      padding: 2vw 0;
      font-family: sans-serif;">
        Jogos
      </h2>
      
      <div class="generos">
        
      <div>
        <button @click="action()">
          Ação
        </button>
        <button @click="terror()">
          terror
        </button>
        
        <button @click="survival()">
          Sobrevivência
        </button>
        <button @click="MA()">
          Mundo aberto
        </button>
      </div>
      </div>

    </div>
  </section>

  <section>
    <transition name="fade" mode="out-in">
  <div v-if="genero == 0">
    <ul class="gayme">
      <li v-for="jogo in jogosAcao" key="jogo.id">
        <img :src="jogo.capa" :alt="jogo.nome">
        <div class="cora">
          <div>
        <p class="nome">{{ jogo.nome }}</p>
        <p class="preco">R${{ jogo.preco.toLocaleString('pt-BR', { minimumFractionDigits: 2 }) }}</p>
        <p class="plataforma">{{ jogo.plataforma }}</p>
        </div>
        <span
  class="fa-heart"
  :class="jogo.favorito ? 'fa-solid favorito' : 'fa-regular fa-heart'"
  @click="toggleFavorito(jogo)"
></span>
        </div>
        <button class="buy">
          <span class="fa-solid fa-cart-shopping"></span><span class="comprar">Comprar</span>
        </button>
      </li>
    </ul>
  </div>
  </transition>
  
  <transition name="fade" mode="out-in">
  <div v-if="genero == 1">
    <ul class="gayme">
      <li v-for="jogo in jogosTerror" key="jogo.id">
        <img :src="jogo.capa" :alt="jogo.nome">
        <div class="cora">
          <div>
        <p class="nome">{{ jogo.nome }}</p>
        <p class="preco">R${{ jogo.preco.toLocaleString('pt-BR', { minimumFractionDigits: 2 }) }}</p>
        <p class="plataforma">{{ jogo.plataforma }}</p>
        </div>
        <span class="fa-regular fa-heart" style="margin-top: 2vw;"></span>
        </div>
        <button class="buy">
          <span
  class="fa-heart"
  :class="jogo.favorito ? 'fa-solid favorito' : 'fa-regular fa-heart'"
  @click="toggleFavorito(jogo)"
></span>
        </button>
      </li>
    </ul>
  </div>
  </transition>
  <transition name="fade" mode="out-in">
  <div v-if="genero == 2">
    <ul class="gayme">
      <li v-for="jogo in jogosSurvival" key="jogo.id">
        <img :src="jogo.capa" :alt="jogo.nome">
        <div class="cora">
          <div>
        <p class="nome">{{ jogo.nome }}</p>
        <p class="preco">R${{ jogo.preco.toLocaleString('pt-BR', { minimumFractionDigits: 2 }) }}</p>
        <p class="plataforma">{{ jogo.plataforma }}</p>
        </div>
        <span
  class="fa-heart"
  :class="jogo.favorito ? 'fa-solid favorito' : 'fa-regular fa-heart'"
  @click="toggleFavorito(jogo)"
></span>
        </div>
        <button class="buy">
          <span class="fa-solid fa-cart-shopping"></span><span class="comprar">Comprar</span>
        </button>
      </li>
    </ul>
  </div>
  </transition>

  <transition name="fade" mode="out-in">
  <div v-if="genero == 3">
    <ul class="gayme">
      <li v-for="jogo in jogosMA" key="jogo.id">
        <img :src="jogo.capa" :alt="jogo.nome">
        <div class="cora" style="display: flex;
        justify-content: space-between  ;">
          <div>
        <p class="nome">{{ jogo.nome }}</p>
        <p class="preco">R${{ jogo.preco.toLocaleString('pt-BR', { minimumFractionDigits: 2 }) }}</p>
        <p class="plataforma">{{ jogo.plataforma }}</p>
      </div>
      <span
  class="fa-heart"
  :class="jogo.favorito ? 'fa-solid favorito' : 'fa-regular fa-heart'"
  @click="toggleFavorito(jogo)"
></span>
      </div>
        <button class="buy">
          <span class="fa-solid fa-cart-shopping"></span><span class="comprar">Comprar</span>
        </button>
      </li>
    </ul>
  </div>
  </transition>

</section>
</div>
<div class="carrinho" v-if="paginas == 1"></div>
</main>

  

</template>


<style scoped>
.fade-enter-active, .fade-leave-active {
  transition: opacity 0.1s;
}
.fade-enter-from, .fade-leave-to {
  opacity: 0.2;
}


main{
  background-color: aliceblue;
}
  ul.gayme{
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    align-items: center;
   
    padding: 2vw 2vw;

  } 

  ul.gayme li{
    width:20.5%;
    padding: 1vw 2vw 2vw 2vw;
  }

  ul.gayme li img{
    width:100%;
    height: 25vw;
    margin-bottom: 0.5vw;
  }

  ul.gayme li p.nome{
    font-size: 0.8rem;
    font-family: 'comfortaa';
  }
  ul.gayme li p.preco{
    font-size: 0.7rem;
    margin: 0.1vw 0;
  }
  ul.gayme li p.plataforma{
    font-size: 0.6rem;
  }
  ul.gayme li button {
    width: 100%;
    text-align: center;
    background-color: #27AE60;
    border: none;
    color: white;
    border-radius:0.5vw ;
    height: 2.5vw;
    font-size: 0.75rem;
    margin-top: 1vw;
    cursor: pointer;
  }
  ul.gayme li button:hover{
    background-color: #1f8b4c;
    transition: 0.2s;
  }

  /*GENEROS */

.generos div{
  display: flex;
  justify-content:center ;
  align-items: center;
}

.generos div button{
  width: 10%;
  height: 5vw;
  font-size: 0.8rem;
  border: none;
  background-color: #3a434a;
  border-radius: 2vw;
  color: white;
  cursor: pointer;
  font-family: 'DM Sans';
  box-shadow: 0.2vw 0.2vw black;
  text-shadow: black 0.1vw 0.1vw;
}
.generos div button:nth-child(2){
  margin: 0 2vw
}
.generos div button:nth-child(3){
  margin-right: 2vw;
}
  .generos div button:hover{
  background-color: #596670;
  width: 11%;
  height: 5.2vw;
  transition: 0.5s;
}

.cora span{
  cursor: pointer;
}
.cora{
  display: flex;
        justify-content: space-between  ;
}



.fa-heart {
  color: #ccc;
  transition: color 0.3s ease;
}

.favorito {
  color: red;
}

</style>