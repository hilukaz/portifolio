<template>
  <div class="header">
    <img v-bind:src="logotipo" class="logotipo">

    <div class="link">
        
      <h3><a href="#sobre" class="as">Sobre</a></h3>
      <h3><a href="#tec" class="as">Tecnologias</a></h3>
      <h3><a href="#projeto" class="as">Projetos</a></h3>
    </div>
      
    <div class="logo">
      <a href="https://github.com/hilukaz"><img v-bind:src="github" alt=""></a>
      <a href="https://www.linkedin.com/in/lucas-hideo-kawakami-ab9601269/"> <img v-bind:src="likendin" alt=""></a>
      <a href="https://wa.me/5511985507008"> <img v-bind:src="what" alt=""></a>
      
     
     
    </div>
  </div>
  
</template>

<script>
/* eslint-disable vue/multi-word-component-names */
export default {
  name: 'Header',
  data(){
    return{
      github:'/logo-github.svg',
      likendin:'/logo-linkedin.svg',
      what:'/logo-whatsapp.svg',
      logotipo:'/code-working.svg'
    }
  }
}
</script>

<style scoped>
.logo{
    display: flex;
    flex-direction: row;
    position: relative;
    
    margin-left: 10px;
    margin-right: 30px;
  }
  .link{
    display: flex;
    flex-direction: row;
    justify-content: end;
    position: relative;
    margin-left: 40%;
  }
  .logotipo{
    min-width:40px;
    max-width: 40px;
    position: relative;
    left: 10px;
  }
  img{
    min-width:40px;
    margin: 0px 15px;
  }
.header{
  display: flex;
  padding: 20px;
  justify-content: space-between;
  border-bottom-width: 12px;
  border-color: gray;
  align-items: center;
  background-color: rgb(230, 231, 231);
  position: fixed;
  width: 100%;
  z-index: 1000;
  height: 4%;
}
.header>h3{
  margin: 5px;
  padding: 0px 20px;
  
}
.as{
  text-decoration: none;
  color: gray;
  text-decoration-style: none;
  
  margin: 0px 30px;
}

@media (max-width: 1270px) {
  /* .header{
    background-color: blue;
  } */
  .link{
    display: none;
  }
}
</style>