<template>
    <div class="introduction-container">
        <div class="introduction-text-container">
            <!-- Pt-Br -->
            <h1 v-if="languagePortuguese" class="introduction-main-text">Prazer em conhecer! <br> Eu me chamo <b
                    class="introduction-name-detail">Lucas Mira</b>, <br> Mas pode me chamar apenas de <b
                    class="introduction-name-detail">Mira</b>
            </h1>
            <!-- En-Us -->
            <h1 v-else class="introduction-main-text">Nice to meet you! <br> My name is <b
                    class="introduction-name-detail">Lucas Mira</b>, <br> But you can just call me <b
                    class="introduction-name-detail">Mira</b>
            </h1>
            <p class="introduction-description">{{ languagePortuguese ? textBR : textUS }}</p>
            <ContactMe class="introduction-contact-class" :languagePortuguese="languagePortuguese" />
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
    props:['languagePortuguese'],
    components: {
        ContactMe
    },
    data(){
        return{
            textBR: 'Desenvolvedor Full-Stack buscando sempre uma nova oportunidade de crescer. Fui exposto à tecnologia desde muito cedo, acredito que esse seja o motivo pelo qual código sempre foi algo tão natural para min. Programação tem sido o meu foco nos últimos 5 anos da minha vida, e espero que continue sendo pelos próximos 50.',
            textUS: 'Full-Stack Developer always looking for a new opportunity to grow. I was exposed to technology from a very early age, I believe this is why coding has always so naturally to me. Programming has been my focus for the last 5 years of my life, and I hope it will continue to be for the next 50.',
        }
    }
}
</script>

<style scoped>
.introduction-container {
    display: flex;
    padding-bottom: 15vh;
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