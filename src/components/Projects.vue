<template>
    <div class="projects-container">
        <div class="projects-title-container">
            <h1>{{languagePortuguese ? 'Projetos' : 'Projects'}}</h1>
            <select v-model="selectedSkill" class="projects-filter">
                <option :value="null">Todos</option>
                <option v-for="skill in skills" :key="skill" :value="skill">{{ skill }}</option>
            </select>
        </div>
        <div class="projects-grid-container">
            <ProjectCard v-for="project in showList" :languagePortuguese="languagePortuguese" :key="project.name" :project="project" />
        </div>
    </div>
</template>

<script>
import ProjectCard from './ProjectCard.vue';

export default {
    name: 'ProjectsComponet',
    props:['languagePortuguese'],
    components: {
        ProjectCard
    },
    data() {
        return {
            selectedSkill: null,
            skills:[
                "HTML/CSS",
                "Javascript",
                'Typescript', 
                "Vue.Js",
                'Nuxt.Js',
                "Python",
                "Django",
                "PHP",
                "Laravel",
                "REST",
                "SQL/Postgresql",
                "MySQL",
                "Figma",
                "Cypress",
            ],
            projectsList: [
                {
                    name: 'Easy-Password',
                    img: require('@/assets/EasyPassword.png'),
                    descBR: 'Se você também está cansado do botão "esqueci a senha", de uma olhada nesse projeto, você vai achar interessante.',
                    descUS: "If you're also tired of the 'forgot password' button, take a look at this project, you'll find it interesting.",
                    skills: ['HTML/CSS', 'Typescript', 'Nuxt.Js', 'Vue.Js', 'Python', 'Django', 'REST', 'SQL/Postgresql', 'Figma', 'Cypress'],
                    projectLink: 'https://easy-password-v2.netlify.app/',
                    codeLinkFront: 'https://github.com/miratkd/easy-password-v2',
                    codeLinkBack: 'https://github.com/miratkd/EasyPasswordBackend',
                    docLinkBack: 'https://documenter.getpostman.com/view/13841210/2sA3kVn2ib'
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
                    name: 'HangMan',
                    img: require('@/assets/hangman.png'),
                    descBR: 'Não tem nada mais simples e relaxante do que uma partida de forca, acerte as letras e você ganha, fique sem vidas e você perde, simples e qualquer um pode experimentar.',
                    descUS: "There's nothing simpler and more relaxing than a hangman match, hit the letters and you win, run out of lives and you lose, simple and anyone can try it.",
                    skills: ['HTML/CSS', 'Javascript', 'Vue.Js', 'PHP', 'Laravel', 'REST', 'MySQL', 'Figma'],
                    projectLink: 'https://hangman-lm.netlify.app/',
                    codeLinkFront: 'https://github.com/miratkd/hangmam-front',
                    codeLinkBack: 'https://github.com/miratkd/hangMan',
                    docLinkBack: 'https://documenter.getpostman.com/view/13841210/2sA3kUG2Es',
                },
                {
                    name: 'Connect-Four',
                    img: require('@/assets/connect-four.png'),
                    descBR: 'Lembra de passar horas jogando connect four quando era criança? Não? Nem eu...',
                    descUS: 'Remember spending hours playing "connect four" when you were a kid? No? Me neither...',
                    skills: ['HTML/CSS', 'Typescript', 'Nuxt.Js', 'Vue.Js', 'Figma', 'Cypress'],
                    projectLink: 'https://connect-four-v2.netlify.app/',
                    codeLinkFront: 'https://github.com/miratkd/connect-four-v2',
                    codeLinkBack: null
                },
                {
                    name: 'Club da Cotação',
                    img: require('@/assets/ClubDaCotacao.png'),
                    descBR: 'Site institucional desenvolvido para a empresa Club da Cotação',
                    descUS: 'Institutional website developed for the company Club da Cotação',
                    skills: ['HTML/CSS', 'Javascript', 'Vue.Js', 'Figma'],
                    projectLink: 'https://club-da-cotacao.netlify.app/',
                    codeLinkFront: null,
                    codeLinkBack: null
                },
                {
                    name: 'My-link',
                    img: require('@/assets/myLink.png'),
                    descBR: 'API para criar uma aplicação de "links cartões de visita"',
                    descUS: 'API to create an application of "business card links"',
                    skills: ['PHP', 'Laravel', 'MySQL', 'REST'],
                    codeLinkBack: 'https://github.com/miratkd/MyLinkBack',
                    docLinkBack: 'https://documenter.getpostman.com/view/13841210/2sA3rwNaFV',
                },
                {
                    name: 'My-kanban',
                    img: require('@/assets/my-kanban.png'),
                    descBR: 'API para criação de um sistema de administração de tarefas "Kanban"',
                    descUS: 'API for creating a "Kanban" task management system',
                    skills: ['PHP', 'Laravel', 'MySQL', 'REST'],
                    codeLinkBack: 'https://github.com/miratkd/my-kanban-back',
                    docLinkBack: 'https://documenter.getpostman.com/view/13841210/2sAXqmB5dr',
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
                },
                {
                    name: 'Black-Jack-Rest',
                    img: require('@/assets/BlackJackRest.png'),
                    descBR: 'Que tal uma partidinha de Black-Jack? (famoso "21")',
                    descUS: 'How about a little game of Black-Jack?',
                    skills: ['HTML/CSS', 'Javascript', 'Vue.Js', 'Python', 'Django', 'REST', 'SQL/Postgresql'],
                    projectLink: 'https://black-jack-rest.netlify.app/',
                    codeLinkFront: 'https://github.com/miratkd/black-jack-rest-front-end',
                    codeLinkBack: 'https://github.com/miratkd/BlackJackRest'
                }
            ]
        }
    },
    computed:{
        showList(){
            if (!this.selectedSkill) return this.projectsList
            return this.projectsList.filter(value => value.skills.includes(this.selectedSkill))
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

.projects-filter{
    padding: 0.5vw;
    border-radius: 10px;
    font-family: 'Space Grotesk';
    font-size: 1.3em;
    cursor: pointer;
}
.projects-filter:focus{
    outline: none;
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