  <script setup>
  import {ref} from 'vue';

  import { jogosAcao, jogosTerror, jogosSurvival, jogosMA } from './cod.js';

    const todosJogos = jogosAcao.concat(jogosMA, jogosSurvival, jogosTerror);
    const listaCarrinho = ref([]);

    for (let jogo of todosJogos) {
    jogo.quantidade = 0
  }

  function adicionarAoCarrinho(jogo) {
    const existe = listaCarrinho.value.find(item => item.id === jogo.id)
    if (existe) {
      existe.quantidade++
    } else {
      listaCarrinho.value.push({ ...jogo, quantidade: 1 })
    }
  }


  

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


    function removerDoCarrinho(item) {
  if (item.quantidade > 1) {
    item.quantidade--;
  } else {
    const index = listaCarrinho.value.findIndex(i => i.id === item.id);
    if (index !== -1) {
      listaCarrinho.value.splice(index, 1);
    }
  }
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
        <li @click="carrinho()">
          <a ><span class="fa-solid fa-cart-shopping"></span></a>
        </li>

        <li >
          <a href=""><span class="fa-solid fa-heart"></span></a>
        </li>

        <li @click="cadastro()">
          <a ><span class="fa-solid fa-user"></span></a>
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
          <button class="buy" @click="adicionarAoCarrinho(jogo)">
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
          <span
    class="fa-heart"
    :class="jogo.favorito ? 'fa-solid favorito' : 'fa-regular fa-heart'"
    @click="toggleFavorito(jogo)"
  ></span>
          </div>
          <button class="buy" @click="adicionarAoCarrinho(jogo)">
            <span class="fa-solid fa-cart-shopping"></span><span class="comprar">Comprar</span>
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
          <button class="buy" @click="adicionarAoCarrinho(jogo)">
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
        <button class="buy" @click="adicionarAoCarrinho(jogo)">
            <span class="fa-solid fa-cart-shopping"></span><span class="comprar">Comprar</span>
          </button>
        </li>
      </ul>
    </div>
    </transition>

  </section>
  </div>
  <div class="carrinho" v-if="paginas == 1">

    <h2 style="text-align: center;
        font-size: 2rem;
        padding: 2vw 0;
        font-family: sans-serif;">Carrinho</h2>

    <div class="localizacao">
      <h3 class="titulo">
        Titulo
      </h3>
      <h3 class="quantidade">
        Quantidade
      </h3>
      <h3 class="subtotal">
        Subtotal
      </h3>
    </div>

    <div v-if="listaCarrinho.length === 0" style="text-align:center; padding: 2vw;">
    Seu carrinho está vazio 
  </div>



  <ul v-else class="pagCarrinho">
    <li v-for="item in listaCarrinho" :key="item.id">
      <div class="tittle-carrinho">
      <img :src="item.capa" :alt="item.nome">
      <div class="nomePlatPrec">
      <h3 class="nmjg">
        {{ item.nome }}
      </h3>
      <h5 class="plataforma-carrinho">
        {{ item.plataforma }}
      </h5>
      <h4 class="preco-carrinho">
        R${{ item.preco.toLocaleString('pt-BR', { minimumFractionDigits: 2 }) }}
      </h4>
    </div>
      </div>

      <div class="quant">
        <button @click="adicionarAoCarrinho(item)" class="add-carrinho">
          +
        </button>
        <h4 class="quant-carrinho">
          {{ item.quantidade }}
        </h4>
        <button @click="removerDoCarrinho(item)" class="subt-carrinho">
          -
        </button>
      </div>
      <div class="subtot">
        R${{ (item.preco * item.quantidade).toLocaleString('pt-BR', { minimumFractionDigits: 2 }) }}
      </div>

    </li>
    <div class="total">
      <div class="descont"> 
        <p>
        <label for="desconto" class="label-desconto">Insira um cupom de desconto</label>
        </p>
        <p>
        <input type="text" class="desc" placeholder="Insira o cupom">
        </p>
      </div>
      <div class="total-final">
      <h2>
    Total: R$ {{
      listaCarrinho.reduce((soma, item) => soma + item.preco * item.quantidade, 0)
      .toLocaleString('pt-BR', { minimumFractionDigits: 2 })
    }}
    </h2>
    <button class="finalizar" @click="listaCarrinho = []">Finalizar</button>
  </div>
  </div>
  </ul>




  </div>
  <div class="cadastro" v-if="paginas == 3">
    <h2 style="text-align: center;
        font-size: 2rem;
        padding: 2vw 0;
        font-family: sans-serif;">
          Cadastro
        </h2>
        <section id="formulario">
          <form action="#" method="get">

            <p class="label"><label for="nm">*Nome</label></p>
            <p class="input"><input type="text" placeholder="Nome"></p>

            <p style="margin-top: 2vw;" class="label"><label for="emai">*E-Mail</label></p>
            <p style="margin-bottom: 2vw;" class="input"><input type="email" placeholder="E-Mail"></p>

            <p class="label"><label for="senha">*Senha</label></p>
            <p class="input"><input type="password" placeholder="Senha"></p>

            <button type="submit">Logar</button>

          </form>
        </section>
  </div>
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
    background-color: white;
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








  /*CARRINHO*/
  ul.pagCarrinho li{
    margin: 0vw 6vw;
    padding: 2vw 3vw;
    display: flex;
    align-items: center;
    width: 80%;
    justify-content: space-between;
    border-bottom: 3px #1f8b4c solid;
    
  }

  ul.pagCarrinho li div.tittle-carrinho{
    display: flex;
    width: 40%;
  }
  ul.pagCarrinho li div.tittle-carrinho img{
    width: 15vw;
    height: 17vw;
  }

  ul.pagCarrinho li div.tittle-carrinho h3{
    font-size: 1.3rem;
  }
  ul.pagCarrinho li div.tittle-carrinho h5{
    font-size: 0.7rem;
    color: #596670;
  }
  ul.pagCarrinho li div.tittle-carrinho h4{
    font-size: 1rem;
  }


  div.quant{
    display: flex;
    align-items: center;
    margin: 0 10.5vw;
    width: 10%;
  }

   div.quant button{
    border: 1px #1f8b4c solid;
    background-color: #27AE60;
    color: white;
    font-size: 1.3rem;
    padding: 0.5vw 1vw;
    width: 100%;
    cursor: pointer;
    text-shadow: black 0.05vw 0.05vw;
  }
  div.quant button:hover{
    background-color: #1f8b4c;
    transition: 0.3s;
  }
  div.quant h4{
    margin: 0 1vw;
  }

  div.localizacao{
    margin: 0vw 6vw;
    padding: 2vw 3vw;
    display: flex;
    align-items: center;
    width: 80%;
    justify-content: space-between;
    border-bottom: #1f8b4c 5px solid;
  }
  div.localizacao .titulo{
    width: 40%;
  }

  div.localizacao .quantidade{
    width: 10%;
  }

  .nomePlatPrec{
    margin-left: 1vw;
  }


  .total{
    display: flex;
    justify-content: space-between;
    margin: 0 6vw;
    align-items: center;
    padding-bottom: 5vw;
  }

  .descont{
    border: #1f8b4c 3px solid;
    margin-top: 4vw;
    padding:1vw 3vw; 
  }


  .descont label{
    font-size: 1rem;
    
  }
  .descont input{
    font-size: 0.5rem;
    border: black 2px solid;
    padding: 0.5vw 1.8vw;
    width: 80%;
  }


  .total .total-final{
    width: 13.1%;
    margin-right: 2vw;
  }
  .total .total-final button{
    background-color: #27AE60;
    border: 2px solid #1f8b4c;
    box-shadow: black 0.1vw 0.1vw;
    font-size: 0.7rem;
    color: white;
    width: 100%;
  }
  .total .total-final h2{
    width: 100%;
  }

  /*FORMULARI */

  #formulario{
    text-align: center;
  }
  #formulario form label{
    width: 20%;
  }
  #formulario form input{
    width: 20%;
    padding: 0.2vw 0.5vw;
    font-size: 0.5rem;
  }

  #formulario form button{
    width: 10%;
    background-color: #27AE60;
    color: white;
    box-shadow: 0.1vw 0.1vw black;
    text-shadow: 0.05vw 0.05vw black;
    padding: 0.2vw 0.5vw;
    font-size: 0.7rem;
    margin-top: 5vw;
  }

  #formulario form button:hover{
    background-color: #1f8b4c;
    transition: 0.3s;
  }


  </style>