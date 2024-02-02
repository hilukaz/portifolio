<template>
  <html>
    <head>
      <title>portifolio</title>
    </head>
    <body>
      <Header/>
      <div class="home">
        <!-- <main>
          <section>projetos</section>
          <section>linguagens</section>
        </main> -->
        <div class="sobre">
          <div class="text">
            <strong><h2>Olá, eu sou</h2></strong>
          </div>
          <h1>Lucas Hideo</h1>
          <div class="text">
            <strong><h2>Programador back-end</h2></strong>
          </div>
        </div>
        <div class="img">
          <img v-bind:src="foto" alt="" class="foto">
        </div>
        <div class="linguagem">
          <Linguagem/>
        </div>
        <div class="projeto"></div>
      </div>
    </body>
  </html>
  
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import Header from '../components/Header.vue'
import Linguagem from '../components/Linguagem.vue'

export default defineComponent({
  name: 'HomeView',
  components:{
    Header,
    Linguagem,
  },
  data(){
    return{
      foto:'/foto2.jpeg',
    }
  }
});


</script>


<style>
  *{
    padding: 0px;
    margin:0px;
  }

  .sobre{
    flex-direction: column;
  }
  

  .home {

    display: grid;
    grid-template-columns: 1fr 1fr;
    /* fr = metade */
    grid-template-rows: 90vh 100vh 100vh;
    /* 100vh é equivalente a tela inteira */
    grid-template-areas:'a a'
    'ling ling' 
    'proj proj';
    /* define quais div ocupam cada coluna */
  }
 
  .home>div{
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .text{
    position: relative;
    left:-20%;
  }

  .text>h2{

  }
  
  .sobre,.img{
    align-items: center;
    justify-content: center;
    
  }

  .linguagem {
    grid-row: 2;
    grid-area: ling;
  }

  .projeto {
    grid-row: 3;
    grid-area: proj;
  }
  .foto{
    max-width: 30%;
    
    border-radius: 50px;
  }
  h1{
    font-size: 5em;
    font-family: 'Lato';
    align-items: center;
    color:rgb(0, 0, 0);
  }
</style>