<template>
    <div class="footer-container">
        <h1>{{ languagePortuguese ? 'Contato' : 'Contact' }}</h1>
        <p class="footer-text">{{ languagePortuguese ? textBR : textUS }}</p>
        <div class="footer-contact-me-container"><ContactMe /></div>
        <div class="footer-line">
            <p class="footer-name-text">LucasMira</p>
            <div class="footer-icons-container">
                <a href="https://www.codewars.com/users/miratkd" target="_blank">
                    <img class="footer-icon" src="@/assets/codeWars2.png" alt="CodeWars">
                </a>
                <a href="https://github.com/miratkd" target="_blank">
                    <img class="footer-icon" src="@/assets/github.svg" alt="GitHub">
                </a>
                <a href="https://www.linkedin.com/in/lucas-mira-17514b203/" target="_blank">
                    <img class="footer-icon" src="@/assets/LinkedIn.svg" alt="LinkId">
                </a>
            </div>
        </div>


        <img class="footer-circle-img" src="@/assets/circle.svg" alt="">
    </div>
</template>

<script>
import ContactMe from './ContactMe.vue';
export default {
    name: 'FooterComponent',
    props:['languagePortuguese'],
    components:{
        ContactMe
    },
    data(){
        return {
            textBR: 'Gostou do meu perfil? Acha que eu me encaixaria no seu projeto? Por favor, entre em contato, eu adoraria conversar e descobrir como posso ajudar o seu projeto a ir para frente.',
            textUS: "Did you like my profile? Do you think I'd fit your bill? Please get in touch, I'd love to chat and find out how I can help your project move forward.",
        }
    }
}
</script>

<style scoped>
.footer-container{
    background: #242424;
    padding: 5vh 10vw;
    margin-top: 15vh;
    position: relative;
}
.footer-text{
    margin-top: 3vh;
    width: 50%;
}
.footer-contact-me-container{
    display: flex;
    justify-content: flex-end;
    margin-top: -2vh;
}
.footer-line{
    display: flex;
    justify-content: space-between;
    margin-top: 6vh;
    border-top: white 1px solid;
    padding-top: 3vh;
}
.footer-name-text{
    font-weight: 700;
    font-size: 2.3em;
}
.footer-icons-container{
    display: flex;
    gap: 2vw;
    margin-right: 3vw;
}
.footer-icon{
    width: 2.5em;
    cursor: pointer;
}
.footer-circle-img {
    position: absolute;
    left: 0;
    bottom: 25%;
    width: 20em;
  }
  @media screen and (max-width: 850px){
    .footer-container{
        text-align: center;
        padding: 2.5vh 10vw;
    }
    .footer-text{
        width: 100%;
    }
    .footer-contact-me-container{
        margin-top: 0;
    }
    .footer-circle-img{
        left: -20%;
        bottom: 35%;
        width: 21em;
    }
  }
</style>