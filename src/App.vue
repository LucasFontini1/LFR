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
  ]
</script>



<template>
  <html>
    

  <header>

    <h1><a href="./App.vue">Games LFR</a></h1>

    <div class="pesquisar">
      <input type="text" placeholder="Pesquisar">
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

      <li>
        <a href="">
          HomePage
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

  <ul>
    <li v-for="jogo in jogosAcao">
      nome: {{ jogo.nome }}
    </li>
  </ul>


  </header>

  
  </html>
</template>


<style scoped>
 
</style>
