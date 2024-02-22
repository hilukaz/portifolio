<template>
    <div class="projeto">
        <h1>Projetos</h1>
        <div class="proj-card">
            <Card v-for="projeto in projetos" :key="projeto.id" :title="projeto.title" :description="projeto.description" :tech="projeto.tech" :imgSrc="projeto.imgSrc"  :livePreviewLink="projeto.livePreviewLink" :viewCodeLink="projeto.viewCodeLink" :hasVideo="projeto.hasVideo" :videoSrc="projeto.videoSrc" />
        </div>

    </div>

    
    <!-- <Card/> -->
    <!-- <div class="proj-card">
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
            // {
            //     id: 2,
            //     title: 'OrganicFlow',
            //     description: 'site que através da tecnologia QrCode possa exibir processos referentes a produção até a distribuição de um determinado alimento',
            //     tech: 'Nodejs, Typescript, PrismaORM',
            //     imgSrc: '/proj-foto/auth-vue.PNG',
            //     livePreviewLink: '###',
            //     viewCodeLink: '##',
            //     videoSrc: null
            // },

            {
                id: 2,
                title: 'Vue_auth',
                description: 'Sistema de autenticação, validação de conta, logout e sessões.',
                tech: 'Vuejs, Nodejs, PrismaORM',
                imgSrc: '/proj-foto/auth-vue.PNG',
                livePreviewLink: 'https://vueauth-frontend.vercel.app/',
                viewCodeLink: 'https://github.com/hilukaz/Vueauth-frontend',
                hasVideo: false,
                videoSrc: null
            },
           
            {
                id: 3,
                title: 'API-USDA',
                description: 'Sistema que utiliza API USDAFood sobre alimentos, permite visualizar as calorias no próprio servidor local',
                tech: 'Nodejs, Typescript, PrismaORM',
                imgSrc: '/proj-foto/API-USDA.PNG',
                livePreviewLink: '###',
                viewCodeLink: '##',
                hasVideo: true,
                videoSrc: '/proj-foto/api.mp4'
            },
            {
                id: 4,
                title: 'CRUD nodejs',
                description: 'CRUD - Create, Read, Update, Delete. Gerenciamento de registros',
                tech: 'Nodejs, Typescript, PrismaORM',
                imgSrc: '/proj-foto/crud.PNG',
                livePreviewLink: '###',
                viewCodeLink: 'https://github.com/hilukaz/prismaORM.git',
                hasVideo: true,
                videoSrc: '/proj-foto/crud.mp4'
            },
            
            {
                id: 5,
                title: 'Chat',
                description: 'Chat bate-papo utilizando socket.io',
                tech: 'Nodejs, Javascript, Socket.io',
                imgSrc: '/proj-foto/chat.PNG',
                livePreviewLink: '###',
                viewCodeLink: 'https://github.com/hilukaz/websocket-chat',
                hasVideo: true,
                videoSrc: '/proj-foto/chat.mp4'
            }
                // {id:2, title:'adaa',description:'adaa', tech:'ada', imgSrc:'/'}
            ],
        }
    }   
});

</script>

<style scoped>
.proj-card{
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    margin:0px 100px;
}
@media (max-width: 1270px) {
    .proj-card{
        justify-content: center;
        margin: 0px;
    }
    h1{
        margin-bottom: 8%;
    }
}
</style>