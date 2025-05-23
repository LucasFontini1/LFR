<script setup>
defineProps(['all-games', 'ac-games', 'terror-games', 'sv-games', 'ma-games',])
defineEmits(['add-cart',''])


</script>

<template>
      <section>
      <transition name="fade" mode="out-in">
    <div v-if="genero == 0">
      <ul class="gayme">
        <li v-for="jogo in ac-games" :key="jogo.id">
          <img :src="jogo.capa" :alt="jogo.nome">
          <div class="cora">
            <div>
          <p class="nome">{{ jogo.nome }}</p>
          <p class="preco">R${{ jogo.preco.toLocaleString('pt-BR', { minimumFractionDigits: 2 }) }}</p>
          <p class="plataforma">{{ jogo.plataforma }}</p>
          </div>

          </div>
          <button class="buy" @click="$emit( 'add-cart')">
            <span class="fa-solid fa-cart-shopping"></span><span class="comprar"> + Carrinho</span>
          </button>
        </li>
      </ul>
    </div>
    </transition>

    <transition name="fade" mode="out-in">
    <div v-if="genero == 1">
      <ul class="gayme">
        <li v-for="jogo in jogosTerror" :key="jogo.id">
          <img :src="jogo.capa" :alt="jogo.nome">
          <div class="cora">
            <div>
          <p class="nome">{{ jogo.nome }}</p>
          <p class="preco">R${{ jogo.preco.toLocaleString('pt-BR', { minimumFractionDigits: 2 }) }}</p>
          <p class="plataforma">{{ jogo.plataforma }}</p>
          </div>

          </div>
          <button class="buy" @click="adicionarAoCarrinho(jogo)">
            <span class="fa-solid fa-cart-shopping"></span><span class="comprar"> + Carrinho</span>
          </button>
        </li>
      </ul>
    </div>
    </transition>
    <transition name="fade" mode="out-in">
    <div v-if="genero == 2">
      <ul class="gayme">
        <li v-for="jogo in jogosSurvival" :key="jogo.id">
          <img :src="jogo.capa" :alt="jogo.nome">
          <div class="cora">
            <div>
          <p class="nome">{{ jogo.nome }}</p>
          <p class="preco">R${{ jogo.preco.toLocaleString('pt-BR', { minimumFractionDigits: 2 }) }}</p>
          <p class="plataforma">{{ jogo.plataforma }}</p>
          </div>

          </div>
          <button class="buy" @click="adicionarAoCarrinho(jogo)">
            <span class="fa-solid fa-cart-shopping"></span><span class="comprar"> + Carrinho</span>
          </button>
        </li>
      </ul>
    </div>
    </transition>

    <transition name="fade" mode="out-in">
    <div v-if="genero == 3">
      <ul class="gayme">
        <li v-for="jogo in jogosMA" :key="jogo.id">
          <img :src="jogo.capa" :alt="jogo.nome">
          <div class="cora" style="display: flex;
          justify-content: space-between  ;">
            <div>
          <p class="nome">{{ jogo.nome }}</p>
          <p class="preco">R${{ jogo.preco.toLocaleString('pt-BR', { minimumFractionDigits: 2 }) }}</p>
          <p class="plataforma">{{ jogo.plataforma }}</p>
        </div>

        </div>
        <button class="buy" @click="adicionarAoCarrinho(jogo)">
            <span class="fa-solid fa-cart-shopping"></span><span class="comprar"> + Carrinho</span>
          </button>
        </li>
      </ul>
    </div>
    </transition>

  </section>
</template>

<style scoped>
.fade-enter-active, .fade-leave-active {
    transition: opacity 0.1s;
  }
  .fade-enter-from, .fade-leave-to {
    opacity: 0.2;
  }
</style>
