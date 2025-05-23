  <script setup>
  import {ref} from 'vue';

  import HeaderComponent from './components/HeaderComponent.vue';
  import GenerosComponent from './components/GenerosComponent.vue';
  import TransitionComponent from './components/TransitionComponent.vue';


 const jogosAcao = [
  {
    id: 1,
    nome: 'Bioshock 1',
    plataforma: 'Ps, Xbox, Pc',
    preco: 25,
    capa: '/img/bioshock.jpg',
    favorito: false,
    quantidade: 0
  },
  {
    id: 2,
    nome: 'The last of us 2',
    plataforma: 'Ps5, Pc',
    preco: 400,
    capa: '/img/tlou.png',
    favorito: false,
    quantidade: 0
  },
  {
    id: 3,
    nome: 'Dead by daylight',
    plataforma: 'Ps, Xbox, Pc',
    preco: 59.99,
    capa: '/img/Dead_By_Daylight.png',
    favorito: false,
    quantidade: 0
  },
  {
    id: 4,
    nome: 'Dying light',
    plataforma: 'Ps, Xbox, Pc',
    preco: 39.99,
    capa: '/img/diyng light.jpg',
    favorito: false,
    quantidade: 0
  },
  {
    id: 5,
    nome: 'Uncharted',
    plataforma: 'Ps, Pc',
    preco: 199.90,
    capa: '/img/uncharted.png',
    favorito: false,
    quantidade: 0
  },
  {
    id: 6,
    nome: 'God Of War',
    plataforma: 'Ps, Pc',
    preco: 199.90,
    capa: '/img/GOW.png',
    favorito: false,
    quantidade: 0
  },
  {
    id: 7,
    nome: 'Far Cry 4',
    plataforma: 'Ps, Xbox, Pc',
    preco: 89.99,
    capa: '/img/farcry.jpg',
    favorito: false,
    quantidade: 0
  },
  {
    id: 8,
    nome: 'Resident Evil 4',
    plataforma: 'Ps, Xbox, Pc',
    preco: 39.99,
    capa: '/img/residentEvil.jpg',
    favorito: false,
    quantidade: 0
  },
]

 const jogosTerror = [
  {
    id: 9,
    nome: 'Outlast',
    plataforma: 'Ps, Xbox, Pc',
    preco: 59.99,
    capa: '/img/outlast.jpg',
    favorito: false,
    quantidade: 0
  },
  {
    id: 10,
    nome: 'Fnaf',
    plataforma: 'Ps5, Pc',
    preco: 75,
    capa: '/img/FNAF.jpg',
    favorito: false,
    quantidade: 0
  },
  {
    id: 11,
    nome: 'Visage',
    plataforma: 'Ps, Xbox, Pc',
    preco: 65.99,
    capa: '/img/visage.jpg',
    favorito: false,
    quantidade: 0
  },
  {
    id: 12,
    nome: 'Phasmophobia',
    plataforma: 'Pc',
    preco: 59.99,
    capa: '/img/phasmophobia.jpg',
    favorito: false,
    quantidade: 0
  },
  {
    id: 13,
    nome: 'Poppy Playtime',
    plataforma: 'Pc',
    preco: 46.99,
    capa: '/img/poppyplaytime.jpg',
    favorito: false,
    quantidade: 0
  },
  {
    id: 14,
    nome: 'Stay out of the house',
    plataforma: 'Pc',
    preco: 59.90,
    capa: '/img/stayoutofthehouse.jpg',
    favorito: false,
    quantidade: 0
  },
  {
    id: 15,
    nome: 'Nun Massacre',
    plataforma: 'Pc',
    preco: 50,
    capa: '/img/nunmassacre.jpg',
    favorito: false,
    quantidade: 0
  },
  {
    id: 16,
    nome: 'Silent Hill',
    plataforma: 'Ps, Xbox, Pc',
    preco: 349.90,
    capa: '/img/silenthill.jpg',
    favorito: false,
    quantidade: 0
  },
]

 const jogosSurvival = [
  {
    id: 17,
    nome: 'Minecraft',
    plataforma: 'Ps, Xbox, Pc',
    preco: 200,
    capa: '/img/minecraft.png',
    favorito: false,
    quantidade: 0
  },
  {
    id: 18,
    nome: 'ARK',
    plataforma: 'Ps5, Xbox, Pc',
    preco: 46.99,
    capa: '/img/ark.jpg',
    favorito: false,
    quantidade: 0
  },
  {
    id: 19,
    nome: 'The Forest',
    plataforma: 'Ps, Xbox, Pc',
    preco: 37.99,
    capa: '/img/forest.jpeg',
    favorito: false,
    quantidade: 0
  },
  {
    id: 20,
    nome: 'No man`s sky',
    plataforma: 'Ps, Xbox, Pc',
    preco: 162,
    capa: '/img/nomanssky.jpg',
    favorito: false,
    quantidade: 0
  },
  {
    id: 21,
    nome: 'Stranded Deep',
    plataforma: 'Ps, Xbox, Pc',
    preco: 37.99,
    capa: '/img/stranded.jpeg',
    favorito: false,
    quantidade: 0
  },
  {
    id: 22,
    nome: 'Subnautica',
    plataforma: 'Ps, Xbox, Pc',
    preco: 124.50,
    capa: '/img/subnautica.png',
    favorito: false,
    quantidade: 0
  },
  {
    id: 23,
    nome: 'Raft',
    plataforma: 'Pc',
    preco: 36.99,
    capa: '/img/raft.jpg',
    favorito: false,
    quantidade: 0
  },
  {
    id: 24,
    nome: 'Green Hell',
    plataforma: 'Ps, Xbox, Pc',
    preco: 16.82,
    capa: '/img/green.jpg',
    favorito: false,
    quantidade: 0
  },
]

 const jogosMA = [
  {
    id: 25,
    nome: 'Red Dead Redemption',
    plataforma: 'Ps, Xbox, Pc',
    preco: 200,
    capa: '/img/rdr2.png',
    favorito: false,
    quantidade: 0
  },
  {
    id: 26,
    nome: 'GTA',
    plataforma: 'Ps5, Xbox, Pc',
    preco: 37,
    capa: '/img/gta.png',
    favorito: false,
    quantidade: 0
  },
  {
    id: 27,
    nome: 'Watch Dogs',
    plataforma: 'Ps, Xbox, Pc',
    preco: 22.49,
    capa: '/img/watchdogs2.png',
    favorito: false,
    quantidade: 0
  },
  {
    id: 28,
    nome: 'Assassin`s Creed',
    plataforma: 'Ps, Xbox, Pc',
    preco: 349.99,
    capa: '/img/ac.jpg',
    favorito: false,
    quantidade: 0
  },
  {
    id: 29,
    nome: 'Spider Man',
    plataforma: 'Ps, Pc',
    preco: 249.90,
    capa: '/img/spiderman.jpg',
    favorito: false,
    quantidade: 0
  },
  {
    id: 30,
    nome: 'Batman Arkham',
    plataforma: 'Ps, Xbox, Pc',
    preco: 89.99,
    capa: '/img/batman.jpg',
    favorito: false,
    quantidade: 0
  },
  {
    id: 31,
    nome: 'DAYZ',
    plataforma: 'Ps, Xbox, Pc',
    preco: 74.99,
    capa: '/img/dayz.jpg',
    favorito: false,
    quantidade: 0
  },
  {
    id: 32,
    nome: 'Fallout',
    plataforma: 'Ps, Xbox, Pc',
    preco: 59.99,
    capa: '/img/fallout.jpg',
    favorito: false,
    quantidade: 0
  },
]


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





    function removerDoCarrinho(item) {
  if (item.quantidade > 1) {
    item.quantidade--;
  } else {
    const index = listaCarrinho.value.find(i => i.id === item.id);
    if (index !== -1) {
      listaCarrinho.value.splice(index, 1);
    }
  }
}


function scrollToTop() {
    window.scrollTo({
      top: 0,
      behavior: 'smooth'
    });
  }

  </script>



  <template>

  <header-component
  @hmpg="hmpg"
  @carrinho="carrinho"
  />


    <main>
      <div class="hmpg" v-if="paginas == 0">
         <h2 class="tittle-main"
        >
          Jogos
        </h2>
        <generos-component
        @acao="action"
        @terror="terror"
        @sobr="survival"
        @ma="MA"
        :genero="genero"
        />

          <transition-component
          :all-games="todosJogos"
          :ac-games="jogosAcao"
          :terror-games="jogosTerror"
          :sv-games="jogosSurvival"
          :ma-games="jogosMA"
          @add-to-cart="adicionarAoCarrinho"

          />
  </div>
  <div class="carrinho" v-if="paginas == 1">

    <h2 class="tittle-main" >Carrinho</h2>

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
      <div>
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
  </main>

  <footer>




<div class="all">


  <div class="contato">
    <p>
      Contatos:
    </p>

    <p >
     <span class="fa-solid fa-clock"></span> 09h às 19h - seg a sex
    </p>

    <span class="fa-solid fa-envelope"></span> gameslfr@gmail.com
  </div>

<img src="/public/img/logo.png" alt="" >
<div>

</div>

</div>

 <hr>
  <div class="direitos">
  <p>

  © 2025 LFR Corporation. Todos os direitos reservados. Todas as marcas são propriedade dos seus respectivos donos no Brasil.

</p>

</div>


<div style="text-align: center; margin-top: 2vw;">
  <button @click="scrollToTop()" class="scroll-top-btn">↑ Voltar ao topo</button>
</div>

  </footer>


  </template>


  <style scoped>



  main{
    background: linear-gradient(135deg, #1e283d, #1c2e44, #2a475e);
    padding-bottom: 5vw;
  }


    ul.gayme{
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
      align-items: center;
      color: aliceblue;
      padding: 2vw 2vw;

    }

    ul.gayme li{
     width: calc(50% - 2vw);
     background: linear-gradient(135deg, #1e283d, #122338, #2a475e);
     box-shadow: 0 0.5vw 1vw rgba(0, 0, 0, 0.5);
     border-radius: 0.8vw;
     margin: 1vw;
      padding: 1vw 2vw 2vw 2vw;
    }

    @media (min-width: 768px) {
  ul.gayme li {
    width: calc(25% - 2vw);
  }
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
      font-weight: bold;
    }
    ul.gayme li p.plataforma{
      font-size: 0.6rem;
    }
    ul.gayme li button {
      width: 100%;
      text-align: center;
      background: linear-gradient(135deg, #19422d, #174d37, #177f4b);
      border: none;
      color: white;
      border-radius:0.5vw ;
      height: 2.5vw;
      font-size: 0.75rem;
      margin-top: 1vw;
      cursor: pointer;
    }
    ul.gayme li button:hover{
      background: linear-gradient(135deg, #51e598, #378f6c, #1c9659);
      transition: 0.2s;

    }










  /*CARRINHO*/
div.carrinho {
  color: aliceblue;
}

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
    padding:2vw 3vw;
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
    width: 14%;
    margin-right: 2vw;
    white-space: nowrap;
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








 main h2.tittle-main{
  text-align: center;
        font-size: 2rem;
        padding: 2vw 0;
        font-family: 'comfortaa';
        color: aliceblue;
 }

  </style>
