<template>
    <div class="projects-container">
        <div class="projects-title-container">
            <h1>{{languagePortuguese ? 'Projetos' : 'Projects'}}</h1>
            <ContactMe :languagePortuguese="languagePortuguese"/>
        </div>
        <div class="projects-grid-container">
            <ProjectCard v-for="project in projectsList" :languagePortuguese="languagePortuguese" :key="project.name" :project="project" />
        </div>
    </div>
</template>

<script>
import ContactMe from './ContactMe.vue';
import ProjectCard from './ProjectCard.vue';

export default {
    name: 'ProjectsComponet',
    props:['languagePortuguese'],
    components: {
        ContactMe,
        ProjectCard
    },
    data() {
        return {
            projectsList: [
                {
                    name: 'Easy-Password',
                    img: require('@/assets/EasyPassword.png'),
                    descBR: 'Se você também está cansado do botão "esqueci a senha", de uma olhada nesse projeto, você vai achar interessante.',
                    descUS: "If you're also tired of the 'forgot password' button, take a look at this project, you'll find it interesting.",
                    skills: ['HTML/CSS', 'Javascript', 'Vue.Js', 'Python', 'Django Rest', 'SQL/Postgresql', 'Figma', 'Cypress'],
                    projectLink: 'https://easypassword-lm.netlify.app/',
                    codeLinkFront: 'https://github.com/miratkd/EasyPasswordFront',
                    codeLinkBack: 'https://github.com/miratkd/EasyPasswordBackend'
                },
                {
                    name: 'Audiphile',
                    img: require('@/assets/audiphile.png'),
                    descBR: 'Um site para mostrar a importância de uma interface na hora de vender alguma coisa.',
                    descUS: 'A website to show the importance of an interface when it comes to selling something.',
                    skills: ['HTML/CSS', 'Javascript', 'Vue.Js', 'Figma'],
                    projectLink: 'https://audiphile.netlify.app/',
                    codeLinkFront: 'https://github.com/miratkd/Audiophile',
                    codeLinkBack: null
                },
                {
                    name: 'Arch',
                    img: require('@/assets/arch.png'),
                    descBR: 'Um projeto voltado para estética, beleza e minimalismo. Meus professores de arte ficariam orgulhosos.',
                    descUS: 'A project focused on aesthetics, beauty and minimalism. My art teachers would be proud.',
                    skills: ['HTML/CSS', 'Javascript', 'Vue.Js', 'Figma'],
                    projectLink: 'https://arch-lm.netlify.app/',
                    codeLinkFront: 'https://github.com/miratkd/Art-Studio?tab=readme-ov-file',
                    codeLinkBack: null
                },
                {
                    name: 'Connect-Four',
                    img: require('@/assets/connect-four.png'),
                    descBR: 'Lembra de passar horas jogando connect four quando era criança? Não? Nem eu...',
                    descUS: 'Remember spending hours playing "connect four" when you were a kid? No? Me neither...',
                    skills: ['HTML/CSS', 'Javascript', 'Vue.Js', 'Figma', 'Cypress'],
                    projectLink: 'https://connect-four-lm.netlify.app/',
                    codeLinkFront: 'https://github.com/miratkd/Connect-Four',
                    codeLinkBack: null
                },
                {
                    name: 'Black-Jack-Rest',
                    img: require('@/assets/BlackJackRest.png'),
                    descBR: 'Que tal uma partidinha de Black-Jack? (famoso "21")',
                    descUS: 'How about a little game of Black-Jack?',
                    skills: ['HTML/CSS', 'Javascript', 'Vue.Js', 'Python', 'Django Rest', 'SQL/Postgresql'],
                    projectLink: 'https://black-jack-rest.netlify.app/',
                    codeLinkFront: 'https://github.com/miratkd/black-jack-rest-front-end',
                    codeLinkBack: 'https://github.com/miratkd/BlackJackRest'
                },
                {
                    name: 'Planets',
                    img: require('@/assets/Planets.png'),
                    descBR: 'Que tal aprender mais um pouquinho sobre os planetas do nosso sistema solar?',
                    descUS: 'How about learning a little more about the planets in our solar system?',
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
    margin-top: 12vh;
}

.projects-title-container {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.projects-grid-container {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 10vh 3vw;
    margin-top: 3vh;
}

@media screen and (max-width: 850px) {
    .projects-container {
        margin: 10vh 3vw;
    }

    .projects-grid-container {
        gap: 10vh 1.5vw;
    }
}

@media screen and (max-width: 450px) {
    .projects-grid-container {
        grid-template-columns: 1fr;
    }
}</style>