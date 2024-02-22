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
        <div class="banner" id="sobre">
          <div class="sobre">
            <div class="text">
              <strong><h2>Olá, eu sou</h2></strong>
            </div>
            <h1>Lucas Hideo</h1>
            <div class="text">
              <strong><h2>Desenvolvedor back-end</h2></strong>
            </div>
          </div>
        
          <div class="img">
            <img v-bind:src="foto" alt="" class="foto">
          </div>
        </div>
        <div class="linguagem" id="tec">
          <!-- essa parte não está responsiva -->
          <Linguagem/>
        </div>
        <div class="projeto" id="projeto">
          <Projeto/>
        </div>
      </div>
    </body>
  </html>
  
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import Header from '../components/Header.vue'
import Linguagem from '../components/Linguagem.vue'
import Projeto from '../components/Projeto.vue'

export default defineComponent({
  name: 'HomeView',
  components:{
    Header,
    Linguagem,
    Projeto
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
  
  #tec, #projeto ,#sobre{

    padding-top: 90px;
  }
  .home {
    display: grid;
    grid-template-columns: 1fr 1fr;
    /* fr = metade */
    grid-template-rows: 100vh 110vh 100vh;
    /* 100vh é equivalente a tela inteira */
    grid-template-areas:'banner banner'
    'ling ling' 
    'proj proj';
    /* define quais div ocupam cada coluna */

    
  }
 
  

  .home>div{
    display: flex;
    justify-content: center;
    /* margin-bottom: 100px ; */
  }

  .text{
    position: relative;
    left:-20%;
  }

  
  .banner{
    align-items: center;
    justify-content: center;
    grid-area: banner;
    
  }

  .img{
    grid-area: img;
    width: 50%;
  }
  .sobre{
    grid-area: sobre;
    width: 50%;
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

  @media screen and (max-width: 1270px) {
  #tec, #projeto, #sobre{
    padding-top: 90px;
  }

  .home {
    
    grid-template-columns: 1fr; 
    grid-template-rows: 100vh 100vh 100vh;
    grid-template-areas:
    'banner'
    'ling ' 
    'proj ';
  }
  .banner, #sobre{
    display: flex;
    flex-direction: column-reverse;
    border-style: double;
    margin: 2%;
    margin-top: 100px;
    padding: 0px;
  }
  .sobre{
    width: 100%;
    margin-top: 50px;
  }
  .foto{
    max-width: 20%;
    min-width: 130px;
  }
  .img{
    padding: 10px;
    width: 100%;
  }
  img{
    max-width: 20%;
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

   

   @media (max-height: 560px) {
      .banner, #sobre{
      display: flex;
      flex-direction: row;
      border-style: double;
      margin: 2%;
      margin-top: 100px;
      padding: 0px;
    }
   }
}
</style>