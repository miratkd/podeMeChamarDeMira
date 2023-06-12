<template>
    <div class="projects-container">
        <div class="projects-title-container">
            <h1>Projetos</h1>
            <ContactMe />
        </div>
        <div class="projects-grid-container">
            <ProjectCard v-for="project in projectsList" :key="project.name" :project="project" />
        </div>
    </div>
</template>

<script>
import ContactMe from './ContactMe.vue';
import ProjectCard from './ProjectCard.vue';

export default {
    name: 'ProjectsComponet',
    components: {
        ContactMe,
        ProjectCard
    },
    data() {
        return {
            projectsList: [
                {
                    name: 'Audiphile',
                    img: require('@/assets/audiphile.png'),
                    desc: 'Um site para mostrar a importância de uma interface na hora de vender alguma coisa.',
                    skills: ['HTML/CSS', 'Javascript', 'Vue.Js'],
                    projectLink: 'https://audiphile.netlify.app/',
                    codeLinkFront: 'https://github.com/miratkd/Audiophile',
                    codeLinkBack: null
                },
                {
                    name: 'Easy-Password',
                    img: require('@/assets/EasyPassword.png'),
                    desc: 'Se você também está cansado do botão "esqueci a senha", de uma olhada nesse projeto, você vai achar interessante.',
                    skills: ['HTML/CSS', 'Javascript', 'Vue.Js', 'Python', 'Django Rest', 'SQL/Postgresql', 'Figma'],
                    projectLink: 'https://easypassword-lm.netlify.app/',
                    codeLinkFront: 'https://github.com/miratkd/EasyPasswordFront',
                    codeLinkBack: 'https://github.com/miratkd/EasyPasswordBackend'
                },
                {
                    name: 'Black-Jack-Rest',
                    img: require('@/assets/BlackJackRest.png'),
                    desc: 'Que tal uma partidinha de Black-Jack? (famoso "21")',
                    skills: ['HTML/CSS', 'Javascript', 'Vue.Js', 'Python', 'Django Rest', 'SQL/Postgresql'],
                    projectLink: 'https://black-jack-rest.netlify.app/',
                    codeLinkFront: 'https://github.com/miratkd/black-jack-rest-front-end',
                    codeLinkBack: 'https://github.com/miratkd/BlackJackRest'
                },
                {
                    name: 'Planets',
                    img: require('@/assets/Planets.png'),
                    desc: 'Que tal aprender mais um pouquinho sobre os planetas do nosso sistema solar?',
                    skills: ['HTML/CSS', 'Javascript', 'Vue.Js', 'Figma'],
                    projectLink: 'https://showplanets.netlify.app/',
                    codeLinkFront: 'https://github.com/miratkd/Planets',
                    codeLinkBack: null
                }
            ]
        }
    }
}
</script>

<style scoped>
.projects-container {
    margin-top: 5vh;
}

.projects-title-container {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.projects-grid-container {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 4vh 3vw;
    margin-top: 3vh;
}
@media screen and (max-width: 850px){
    .projects-container {
        margin: 0 3vw;
    }
    .projects-grid-container{
        gap: 4vh 1.5vw;
    }
}
@media screen and (max-width: 450px){
    .projects-grid-container {
        grid-template-columns: 1fr;
    }
}</style>