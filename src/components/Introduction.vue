<template>
    <div class="introduction-container">
        <div class="introduction-text-container">
            <h1 class="introduction-main-text">Prazer em conhecer! <br> Eu me chamo <b
                    class="introduction-name-detail">Lucas Mira</b>, <br> Mas pode me chamar apenas de <b
                    class="introduction-name-detail">Mira</b></h1>
            <p class="introduction-description">Based in the UK, I’m a front-end developer passionate about building
                accessible web apps that users love.</p>
            <ContactMe class="introduction-contact-class" />
        </div>
        <div class="introduction-img-container">
            <img class="introduction-img-oval" src="@/assets/oval.svg" alt="">
            <img class="introduction-img" src="@/assets/photo.png" alt="">

        </div>

    </div>
</template>

<script>
import ContactMe from './ContactMe.vue';
export default {
    name: 'IntroductionComponent',
    components: {
        ContactMe
    }
}
</script>

<style scoped>
.introduction-container {
    display: flex;
    padding-bottom: 7vh;
}

.introduction-text-container {
    width: 55%;
    display: flex;
    flex-direction: column;
    justify-content: center;
}

.introduction-img-container {
    width: 45%;
    position: relative;
}

.introduction-img {
    width: 100%;
}

.introduction-main-text {
    width: 120%;
    z-index: 2;
}

.introduction-name-detail {
    text-decoration: underline;
    text-decoration-color: #4EE1A0;
}

.introduction-description {
    margin-top: 4vh;
}

.introduction-contact-class {
    margin-top: 3vh;
}

.introduction-img-oval {
    position: absolute;
    margin-top: 110%;
    width: 8em;
    margin-left: -11%;
}

@media screen and (max-width: 850px) {
    .header-container {
        width: 100%;
    }

    .introduction-text-container {
        margin-top: 10vh;
        padding-left: 3vw;
        width: 65%;
    }

    .introduction-img-oval {
        position: absolute;
        margin-top: 122%;
        width: 8em;
        margin-left: -15%;
    }
}
@media screen and (max-width: 450px){
    .introduction-container{
        flex-direction: column-reverse;
        align-items: center;
    }
    .introduction-img-container{
        width: 65%;
    }
    .introduction-img-oval{
        margin-top: 122%;
        width: 8em;
        margin-left: unset;
        right: -15%;
    }
    .introduction-text-container {
        margin-top: 5vh;
        padding-left: 0;
        width: 90%;
        text-align: center;
    }
    .introduction-main-text{
        width: 100%;
    }
    .introduction-contact-class {
        margin: 0 auto;
        margin-top: 3vh;
    }
}
</style>