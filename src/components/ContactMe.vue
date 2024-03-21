<template>
    <a href="https://www.linkedin.com/in/lucas-mira-17514b203/" target="_blank" class="contact-p">
        {{languagePortuguese ? 'ENTRAR EM CONTATO' : 'CONTACT ME'}}
    </a>
</template>

<script>
export default {
    name: 'ContactMeComponent',
    props:['languagePortuguese']
}
</script>

<style scoped>
.contact-p {
    border-bottom: #4EE1A0 0.2em solid;
    text-decoration: none;
    padding-bottom: 1vh;
    width: fit-content;
    cursor: pointer;
    font-family: 'Space Grotesk';
    margin: 0;
    font-size: 1.3em;
    color: white;
    margin-top: 3.5vh;
}
</style>