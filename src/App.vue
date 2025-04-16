<script setup>
  const jogosAcao = [
    {
      id: 1,
      nome: 'Bioshock 1',
      plataforma: 'Ps, Xbox, Pc',
      preco: 25,
      capa: ''
    },
    {
      id: 2,
      nome: 'The last of us 2 Remastered',
      plataforma: 'Ps5, Pc',
      preco: 400,
      capa: ''
    },
    {
      id: 3,
      nome: 'Dead by daylihght',
      plataforma: 'Ps, Xbox, Pc',
      preco: 59.99,
      capa: ''
    },
    {
      id: 4,
      nome: 'Dying light',
      plataforma: 'Ps, Xbox, Pc',
      preco: 39.99,
      capa: ''
    },
    {
      id: 5,
      nome: 'Uncharted',
      plataforma: 'Ps, Pc',
      preco: 199.90,
      capa: ''
    },
    {
      id: 6,
      nome: 'God Of War',
      plataforma: 'Ps, Pc',
      preco: 199.90,
      capa: ''
    },
    {
      id: 7,
      nome: 'Far Cry 4',
      plataforma: 'Ps, Xbox, Pc',
      preco: 89.99,
      capa: ''
    },
    {
      id: 8,
      nome: 'Resident Evil 4',
      plataforma: 'Ps, Xbox, Pc',
      preco: 39.99,
      capa: ''
    },
  ]

  const jogosTerror = [
    {
      id: 1,
      nome: 'Outlast',
      plataforma: 'Ps, Xbox, Pc',
      preco: ,
      capa: ''
    },
    {
      id: 2,
      nome: 'Fnaf',
      plataforma: 'Ps5, Pc',
      preco: 75,
      capa: ''
    },
    {
      id: 3,
      nome: 'Visage',
      plataforma: 'Ps, Xbox, Pc',
      preco: 65.99,
      capa: ''
    },
    {
      id: 4,
      nome: 'Phasmophobia',
      plataforma: 'Pc',
      preco: 59.99,
      capa: ''
    },
    {
      id: 5,
      nome: 'Poppy Playtime',
      plataforma: 'Pc',
      preco: 46.99,
      capa: ''
    },
    {
      id: 6,
      nome: 'Stay out of the house',
      plataforma: 'Pc',
      preco: 59.90,
      capa: ''
    },
    {
      id: 7,
      nome: 'Nun Massacre',
      plataforma: 'Pc',
      preco: 50,
      capa: ''
    },
    {
      id: 8,
      nome: 'Silent Hill',
      plataforma: 'Ps, Xbox, Pc',
      preco: 349.90,
      capa: ''
    },
  ]

  const jogosSurvival = [
    {
      id: 1,
      nome: 'Minecraft',
      plataforma: 'Ps, Xbox, Pc',
      preco: 200,
      capa: ''
    },
    {
      id: 2,
      nome: 'ARK',
      plataforma: 'Ps5, Xbox, Pc',
      preco: 46.99,
      capa: ''
    },
    {
      id: 3,
      nome: 'The Forest',
      plataforma: 'Ps, Xbox, Pc',
      preco: 37.99,
      capa: ''
    },
    {
      id: 4,
      nome: 'No man`s sky',
      plataforma: 'Ps, Xbox, Pc',
      preco: 162,
      capa: ''
    },
    {
      id: 5,
      nome: 'Stranded Deep',
      plataforma: 'Ps, Xbox, Pc',
      preco: 37.99,
      capa: ''
    },
    {
      id: 6,
      nome: 'Subnautica',
      plataforma: 'Ps, Xbox, Pc',
      preco: 124.50,
      capa: ''
    },
    {
      id: 7,
      nome: 'Raft',
      plataforma: 'Pc',
      preco: 36.99,
      capa: ''
    },
    {
      id: 8,
      nome: 'Green Hell',
      plataforma: 'Ps, Xbox, Pc',
      preco: 16.82,
      capa: ''
    },
  ]

  const jogosMA = [
    {
      id: 1,
      nome: 'Red Dead Redemption',
      plataforma: 'Ps, Xbox, Pc',
      preco: 200,
      capa: ''
    },
    {
      id: 2,
      nome: 'GTA',
      plataforma: 'Ps5, Xbox, Pc',
      preco: 37,
      capa: ''
    },
    {
      id: 3,
      nome: 'Watch Dogs',
      plataforma: 'Ps, Xbox, Pc',
      preco: 22.49,
      capa: ''
    },
    {
      id: 4,
      nome: 'Assassin`s Creed',
      plataforma: 'Ps, Xbox, Pc',
      preco: 349.99,
      capa: ''
    },
    {
      id: 5,
      nome: 'Spider Man',
      plataforma: 'Ps, Pc',
      preco: 249.90,
      capa: ''
    },
    {
      id: 6,
      nome: 'Batman Arkham',
      plataforma: 'Ps, Xbox, Pc',
      preco: 89.99,
      capa: ''
    },
    {
      id: 7,
      nome: 'DAYZ',
      plataforma: 'Ps, Xbox, Pc',
      preco: 74.99,
      capa: ''
    },
    {
      id: 8,
      nome: 'Fallout',
      plataforma: 'Ps, Xbox, Pc',
      preco: 59,99,
      capa: ''
    },
  ]
</script>



<template>
  <html>
    

  <header>

    <h1><a href="./App.vue">Games LFR</a></h1>

    <div class="pesquisar">
      <input type="text" placeholder="Pesquisar" >
      <span class="fa-solid fa-magnifying-glass"></span>
   
    
    </div>
    <div style="display: flex; align-items: center;">
    <ul class="ulPrincipal">
      <li>
        <a href="">
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
      <li>
        <a href=""><span class="fa-solid fa-cart-shopping"></span></a>
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
  
  <ul>
    <li v-for="jogo in jogosAcao">
      nome: {{ jogo.nome }}
    </li>
  </ul>
  
  <ul>
    <li v-for="jogo in jogosTerror">
      nome: {{ jogo.nome }}
    </li>
  </ul>

  <ul>
    <li v-for="jogo in jogosSurvival">
      nome: {{ jogo.nome }}
    </li>
  </ul>

  <ul>
    <li v-for="jogo in jogosMA">
      nome: {{ jogo.nome }}
    </li>
  </ul>
  
  </html>
</template>


<style scoped>
 
</style>
