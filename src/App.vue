<script setup>
  const jogosAcao = [
    {
      id: 1,
      nome: 'Bioshock 1',
      plataforma: 'Ps, Xbox, Pc',
      preco: 25,
      capa: 'public/img/bioshock.jpg'
    },
    {
      id: 2,
      nome: 'The last of us 2 Remastered',
      plataforma: 'Ps5, Pc',
      preco: 400,
      capa: 'public/img/tlou.png'
    },
    {
      id: 3,
      nome: 'Dead by daylihght',
      plataforma: 'Ps, Xbox, Pc',
      preco: 59.99,
      capa: 'public/img/Dead_By_Daylight.png'
    },
    {
      id: 4,
      nome: 'Dying light',
      plataforma: 'Ps, Xbox, Pc',
      preco: 39.99,
      capa: 'public/img/diyng light.jpg'
    },
    {
      id: 5,
      nome: 'Uncharted',
      plataforma: 'Ps, Pc',
      preco: 199.90,
      capa: 'public/img/uncharted.png'
    },
    {
      id: 6,
      nome: 'God Of War',
      plataforma: 'Ps, Pc',
      preco: 199.90,
      capa: 'public/img/GOW.png'
    },
    {
      id: 7,
      nome: 'Far Cry 4',
      plataforma: 'Ps, Xbox, Pc',
      preco: 89.99,
      capa: 'public/img/farcry.jpg'
    },
    {
      id: 8,
      nome: 'Resident Evil 4',
      plataforma: 'Ps, Xbox, Pc',
      preco: 39.99,
      capa: 'public/img/residentEvil.jpg'
    },
  ]

  const jogosTerror = [
    {
      id: 1,
      nome: 'Outlast',
      plataforma: 'Ps, Xbox, Pc',
      preco: 59.99,
      capa: 'public/img/outlast.jpg'
    },
    {
      id: 2,
      nome: 'Fnaf',
      plataforma: 'Ps5, Pc',
      preco: 75,
      capa: 'public/img/FNAF.jpg'
    },
    {
      id: 3,
      nome: 'Visage',
      plataforma: 'Ps, Xbox, Pc',
      preco: 65.99,
      capa: 'public/img/visage.jpg'
    },
    {
      id: 4,
      nome: 'Phasmophobia',
      plataforma: 'Pc',
      preco: 59.99,
      capa: 'public/img/phasmophobia.jpg'
    },
    {
      id: 5,
      nome: 'Poppy Playtime',
      plataforma: 'Pc',
      preco: 46.99,
      capa: 'public/img/poppyplaytime.jpg'
    },
    {
      id: 6,
      nome: 'Stay out of the house',
      plataforma: 'Pc',
      preco: 59.90,
      capa: 'public/img/stayoutofthehouse.jpg'
    },
    {
      id: 7,
      nome: 'Nun Massacre',
      plataforma: 'Pc',
      preco: 50,
      capa: 'public/img/nunmassacre.jpg'
    },
    {
      id: 8,
      nome: 'Silent Hill',
      plataforma: 'Ps, Xbox, Pc',
      preco: 349.90,
      capa: 'public/img/silenthill.jpg'
    },
  ]

  const jogosSurvival = [
    {
      id: 1,
      nome: 'Minecraft',
      plataforma: 'Ps, Xbox, Pc',
      preco: 200,
      capa: 'public/img/minecraft.png'
    },
    {
      id: 2,
      nome: 'ARK',
      plataforma: 'Ps5, Xbox, Pc',
      preco: 46.99,
      capa: 'public/img/ark.jpg'
    },
    {
      id: 3,
      nome: 'The Forest',
      plataforma: 'Ps, Xbox, Pc',
      preco: 37.99,
      capa: 'public/img/theforest.jpg'
    },
    {
      id: 4,
      nome: 'No man`s sky',
      plataforma: 'Ps, Xbox, Pc',
      preco: 162,
      capa: 'public/img/nomanssky.jpg'
    },
    {
      id: 5,
      nome: 'Stranded Deep',
      plataforma: 'Ps, Xbox, Pc',
      preco: 37.99,
      capa: 'public/img/strandeddeep.jpg'
    },
    {
      id: 6,
      nome: 'Subnautica',
      plataforma: 'Ps, Xbox, Pc',
      preco: 124.50,
      capa: 'public/img/subnautica.png'
    },
    {
      id: 7,
      nome: 'Raft',
      plataforma: 'Pc',
      preco: 36.99,
      capa: 'public/img/raft.jpg'
    },
    {
      id: 8,
      nome: 'Green Hell',
      plataforma: 'Ps, Xbox, Pc',
      preco: 16.82,
      capa: 'public/img/greenhell.jpg'
    },
  ]

  const jogosMA = [
    {
      id: 1,
      nome: 'Red Dead Redemption',
      plataforma: 'Ps, Xbox, Pc',
      preco: 200,
      capa: 'public/img/rdr2.png'
    },
    {
      id: 2,
      nome: 'GTA',
      plataforma: 'Ps5, Xbox, Pc',
      preco: 37,
      capa: 'public/img/gta.png'
    },
    {
      id: 3,
      nome: 'Watch Dogs',
      plataforma: 'Ps, Xbox, Pc',
      preco: 22.49,
      capa: 'public/img/watchdogs2.png'
    },
    {
      id: 4,
      nome: 'Assassin`s Creed',
      plataforma: 'Ps, Xbox, Pc',
      preco: 349.99,
      capa: 'public/img/ac.jpg'
    },
    {
      id: 5,
      nome: 'Spider Man',
      plataforma: 'Ps, Pc',
      preco: 249.90,
      capa: 'public/img/spiderman.jpg'
    },
    {
      id: 6,
      nome: 'Batman Arkham',
      plataforma: 'Ps, Xbox, Pc',
      preco: 89.99,
      capa: 'public/img/batman.jpg'
    },
    {
      id: 7,
      nome: 'DAYZ',
      plataforma: 'Ps, Xbox, Pc',
      preco: 74.99,
      capa: 'public/img/dayz.jpg'
    },
    {
      id: 8,
      nome: 'Fallout',
      plataforma: 'Ps, Xbox, Pc',
      preco: 59.99,
      capa: 'public/img/fallout.jpg'
    },
  ]
</script>



<template>
  <html>
    

  <header>

    <h1><a href="./App.vue"><img src="/public/img/logo.png" alt="GAMES LFR"></a></h1>

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
  
  <ul class="gayme">
    <li v-for="jogo in jogosAcao">
      <img :src="jogo.capa" :alt="jogo.nome">
    </li>
  </ul>
  

  
  </html>
</template>


<style scoped>
  ul.gayme{
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    justify-content: space-between;
    
  }

  ul.gayme li{
    width:25%;
  }

  ul.gayme li img{
    width:80%;
    height: 20vw;
  }

</style>
