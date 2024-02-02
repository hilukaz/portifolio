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
          <!-- essa parte não está responsiva -->
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
    grid-template-rows: 100vh 100vh 100vh;
    /* 100vh é equivalente a tela inteira */
    grid-template-areas:'sobre img'
    'ling ling' 
    'proj proj';
    /* define quais div ocupam cada coluna */

    
  }
 
  

  .home>div{
    display: flex;
    justify-content: center;
    margin-bottom: 100px ;
  }

  .text{
    position: relative;
    left:-20%;
  }

  
  .sobre,.img{
    align-items: center;
    justify-content: center;
    
  }

  .img{
    grid-area: img;
  }
  .sobre{
    grid-area: sobre;
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

  @media screen and (max-width: 600px) {
  .home {
    grid-template-columns: 1fr; /* Remova esta linha para ter uma única coluna em dispositivos móveis */
    grid-template-rows: 60vh;
    grid-template-areas:
    'img' 
    'sobre'
    'ling ' 
    'proj ';
  }
  .img{
    padding: 10px;
  }
  img{
    min-width: 50%;
  }
  h1{
    font-size: 3em;
    font-family: 'Lato';
    align-items: center;
    color:rgb(0, 0, 0);
  }
  .home>div{
    display: flex;
    justify-content: center;
    margin-bottom: 0px ;
   }
   h2{
    font-size: 1em;
   }
}
</style>