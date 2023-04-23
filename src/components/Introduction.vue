<template>
    <div class="introduction-container">
        <div class="introduction-text-container">
            <h1 class="introduction-main-text">Prazer em conhecer! <br> Eu me chamo <b class="introduction-name-detail">Lucas Mira</b>, <br> Mas pode me chamar apenas de <b class="introduction-name-detail">Mira</b></h1>
        </div>
        <img class="introduction-img" src="@/assets/photo.png" alt="">
    </div>
</template>

<script>
export default {
    name: 'IntroductionComponent'
}
</script>

<style scoped>
.introduction-container{
    display: flex;
}
.introduction-text-container{
    width: 55%;
    display: flex;
    flex-direction: column;
    justify-content: center;
}
.introduction-img{
    width: 45%;
}
.introduction-main-text{
    width: 120%;
    z-index: 2;
}
.introduction-name-detail{
    text-decoration: underline;
    text-decoration-color: #4EE1A0;
}
</style>