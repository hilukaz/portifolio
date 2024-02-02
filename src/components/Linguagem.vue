<template>
    <div class="ling">
        <h1>Tecnologias</h1>
        <h2>tecnologias que trabalho recentemente</h2>
        <div class="tec">
            <img src="../assets/logo/html.png" alt="">
            <img src="../assets/logo/css-3.png" alt="css">
            <img src="../assets/logo/js.png" alt="javascript">
            <img src="../assets/logo/typescript.png" alt="typescript">
            <img src="../assets/logo/nodejs.svg" alt="nodejs">
            <img src="../assets/logo/mysql.png" alt="">
            <img src="../assets/logo/prisma_logo-freelogovectors.net_.png" alt="">
            <img src="../assets/logo/planetscale-logo-0EEA8CAEB4-seeklogo.com.png" alt="">
            <img src="../assets/logo/vue.png" alt="">
            <img src="../assets/logo/laravel.png" alt="">
        </div>
    </div>
</template>

<script>
/* eslint-disable */
export default{
    name:'Linguagem',
    data(){

    }
}

</script>

<style scoped>
img{
    max-height: 100px;
    margin: 50px;
    min-height: 10px;
}
.tec{
    display: flex;
    padding: 100px;
    flex-wrap: wrap;
}
.ling{
    background-color: aqua;
}
</style>