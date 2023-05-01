<template>
    <div>
        <div class="project-card-container">
            <img class="project-card-img" :src="project.img" alt="">
            <div class="project-card-img-info-container">
                <p v-if="project.projectLink" v-on:click="goToLink(project.projectLink)" class="project-card-img-info-text">Ver Projeto</p>
                <p v-if="project.codeLinkFront" v-on:click="goToLink(project.codeLinkFront)" class="project-card-img-info-text">Ver Código Front-End</p>
                <p v-if="project.codeLinkBack" v-on:click="goToLink(project.codeLinkBack)" class="project-card-img-info-text">Ver Código Back-End</p>
            </div>
        </div>
        
        <h6 class="project-title">{{project.name}}</h6>
        <p class="project-desc">{{project.desc}}</p>
        <div class="project-card-skills-conatiner">
            <p v-for="(skill, idx) in project.skills" :key="idx">{{skill}}</p>
        </div>
    </div>
</template>

<script>
export default {
    name: 'ProjectCardComponent',
    props: ['project'],
    methods:{
        goToLink (link) { window.open(link, '_blank'); }
    }
}
</script>

<style scoped>
.project-card-img{
    width: 100%;
    transition: filter 0.3s;
}
.project-card-container:hover > .project-card-img{
    filter: brightness(15%)
}
.project-card-container:hover > .project-card-img-info-container{
    opacity: 1;
}
.project-card-img-info-container{
    position: absolute;
    top: 0;
    left: 0;
    height: 100%;
    width: 100%;
    transition:  opacity 0.3s linear;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    gap: 10%;
    display: flex;
    opacity: 0;
}
.project-card-skills-conatiner{
    display: flex;
    gap: 0.5vh 2vw;
    flex-wrap: wrap;
}
.project-title{
    margin: 1.5vh 0;
}
.project-desc{
    margin-bottom: 3vh;
}
.project-card-container{
    position: relative;
    width: 100%;
}
.project-card-img-info-text{
    font-weight: 700;
    padding-bottom: 1vh;
    border-bottom: 0.5vh solid #4EE1A0;
    cursor: pointer;
}
</style>