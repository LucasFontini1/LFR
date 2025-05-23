<script setup>
defineEmits(['acao', 'terror', 'sobr', 'ma'])
defineProps(['genero'])
</script>

<template>
   <section >
      <div>
        <div class="generos">

        <div>
          <button v-if="genero !== 0" @click="$emit('acao')">
            Ação
          </button>
          <button  class="selected" v-else @click="$emit('acao')">
            Ação
          </button>


          <button v-if="genero !== 1" @click="$emit('terror')">
            Terror
          </button>
          <button class="selected" v-else @click="$emit('terror')">
            Terror
          </button>


          <button v-if="genero !== 2" @click="$emit('sobr')">
            Sobrevivência
          </button>
          <button class="selected" v-else @click="$emit('sobr')">
            Sobrevivência
          </button>


          <button v-if="genero !== 3" @click="$emit('ma')">
            Mundo Aberto
          </button>
          <button class="selected" v-else @click="$emit('ma')">
            Mundo Aberto
          </button>
        </div>
        </div>

      </div>
    </section>
</template>

<style scoped>
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
    border: 1px solid #2a375e;
    background-color: #171a21;
    border-radius: 2vw;
    color: aliceblue;
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
   .generos button.selected{
  border: aliceblue 1px solid;
 }
</style>
