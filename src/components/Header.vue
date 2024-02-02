<template>
  <div class="header">
    <img v-bind:src="logotipo" class="logotipo">

    <div class="link">
      
    <h3><a href="#">Sobre</a></h3>
    <h3><a href="##">Tecnologias</a></h3>
    <h3><a href="###">Projetos</a></h3>
    </div>
      
    <div class="logo">
      <img v-bind:src="github" alt="">
      <img v-bind:src="likendin" alt="">
      <img v-bind:src="what" alt="">
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
  }
  .link{
    display: flex;
    flex-direction: row;
    justify-content: end;
    position: relative;
    margin-left: 50%;
  }
  .logotipo{
    min-width:40px;
    max-width: 40px;
    position: relative;
    left: 10px;
  }
  .logo>img{
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
}
.header>h3{
  margin: 5px;
  padding: 0px 20px;
  
}
a{
  text-decoration: none;
  color: gray;
  text-decoration-style: none;
  
  margin: 0px 30px;
}

</style>