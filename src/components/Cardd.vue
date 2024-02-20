<template>
<div class="project-card">
  <img v-bind:src="imgSrc" alt="">
  <h2 class="project-title">{{ title }}</h2>
  <p class="project-description">{{description}}</p>
  <p class="tech-stack">Tecnologias: {{tech}}</p>
  <div class="project-actions">
    <div v-if="hasVideo">
        <button @click="showVideo" class="preview-button">Live Preview</button>
      </div>
    <a v-else :href="livePreviewLink" class="preview-button">Live Preview</a>
 
    <a :href="viewCodeLink" class="view-code-button">View Code</a>
  
  </div>
  <div v-if="showingVideo" class="video-overlay">
      <div class="video-container">
        <video controls :src="videoSrc" class="video-player"></video>
      </div>
      <button @click="hideVideo" class="close-button">Fechar Vídeo</button>
    </div>
</div>
</template>

<script>
/* eslint-disable */
export default({
    name:'Cardd',
    props:{
      title:String,
      description:String,
      tech:String,
      imgSrc:String,
      livePreviewLink: String, // Adicione isso se você tiver um link de pré-visualização ao vivo
      viewCodeLink: String,
      hasVideo: Boolean,
      videoSrc: String
    },
    methods: {
      showVideo() {
        // Adicione a lógica para exibir o vídeo
        this.showingVideo = true;

      },
      hideVideo(){
        this.showingVideo=false;
      }
    },
    data(){
      return{
        showingVideo:false
      }
    }
})
</script>
<style scoped>
.video-overlay {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.5); /* Opacidade de 50% */
  z-index: 1000;
  display: flex;
  justify-content: center;
  align-items: center;
}

.video-container {
  max-width: 80%;
  max-height: 80%;
}

.video-player {
  width: 80%;
  height: 80%;
}

.close-button {
  position: absolute;
  top: 10px;
  right: 10px;
  background-color: transparent;
  border: none;
  color: white;
  font-size: 16px;
  cursor: pointer;
}

.project-card {
  width: 300px;
  background-color: #fff;
  border-radius: 5px;
  /* box-shadow: 2px 2px 5px 5px rgba(0, 0, 0, 1); */
  border-style: double;
  padding: 20px;
  margin-bottom: 20px;
    margin: 50px;
}
img{
  max-height: 180px;
  max-width: 100%;
    margin-bottom: 30px;
    min-height: 10px;
}

.project-title {
  font-size: 24px;
  margin-bottom: 10px;
}

.project-description {
  font-size: 16px;
  line-height: 1.5;
  margin-bottom: 20px;
  height: 96.042px;
}

.tech-stack {
  font-size: 14px;
  color: #666;
  margin-bottom: 20px;
}

.project-actions {
  display: flex;
  justify-content: space-between;
   
}

.preview-button,
.view-code-button {
  display: block;
  width: 100px;
  height: 40px;
  line-height: 40px;
  text-align: center;
  border-radius: 5px;
  text-decoration: none;
  color: #fff;
  font-size: 14px;
  border: none;
}

.preview-button {
  background-color: #f04;
}

.view-code-button {
  background-color: #333;
} 
</style>