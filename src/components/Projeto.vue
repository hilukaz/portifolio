<template>
    <div class="projeto">
        <h1>Projetos</h1>
        <div class="tec">
            <Card v-for="projeto in projetos" :key="projeto.id" :title="projeto.title" :description="projeto.description" :tech="projeto.tech" :imgSrc="projeto.imgSrc"  :livePreviewLink="projeto.livePreviewLink" :viewCodeLink="projeto.viewCodeLink" :hasVideo="projeto.hasVideo" :videoSrc="projeto.videoSrc" />
        </div>

    </div>

    
    <!-- <Card/> -->
    <!-- <div class="tec">
        <Card/>
    </div> -->
</template>

<script lang="ts">

/* eslint-disable */
import Card from './Cardd.vue'

import { defineComponent } from 'vue';
export default defineComponent({
  name: 'Projeto',             
  components:{
    Card
  },
  data(){
        return{
            projetos:[
            {
                id: 1,
                title: 'OrganicFlow',
                description: 'site que através da tecnologia QrCode possa exibir processos referentes a produção até a distribuição de um determinado alimento',
                tech: 'Nodejs, Typescript, PrismaORM',
                imgSrc: '/proj-foto/auth-vue.PNG',
                livePreviewLink: '###',
                viewCodeLink: '##',
                videoSrc: null
            },

            {
                id: 2,
                title: 'Vue_auth',
                description: 'Sistema de autenticação, validação de conta, logout e sessões.',
                tech: 'Nodejs, Typescript, PrismaORM',
                imgSrc: '/proj-foto/auth-vue.PNG',
                livePreviewLink: 'https://vueauth-frontend.vercel.app/',
                viewCodeLink: '##',
                hasVideo: false,
                videoSrc: null
            },
           
            {
                id: 3,
                title: 'API-USDA',
                description: 'sistema que utiliza API USDAFood sobre alimentos, permite visualizar as calorias no próprio servidor local',
                tech: 'Nodejs, Typescript, PrismaORM',
                imgSrc: '/proj-foto/API-USDA.PNG',
                livePreviewLink: '###',
                viewCodeLink: '##',
                hasVideo: true,
                videoSrc: '/proj-foto/api.mp4'
            }
                // {id:2, title:'adaa',description:'adaa', tech:'ada', imgSrc:'/'}
            ],
        }
    }   
});

</script>

<style scoped>
.tec{
    display: flex;
    padding: 100px;
    flex-wrap: wrap;
}

</style>