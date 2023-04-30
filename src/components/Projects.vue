<template>
    <div class="projects-container">
        <div class="projects-title-container">
            <h1>Projetos</h1>
            <ContactMe/>
        </div>
        <div class="projects-grid-container">
            <ProjectCard/>
            <ProjectCard/>
            <ProjectCard/>
        </div>
    </div>
</template>

<script>
import ContactMe from './ContactMe.vue';
import ProjectCard from './ProjectCard.vue';

export default {
    name: 'ProjectsComponet',
    components:{
        ContactMe,
        ProjectCard
    }
}
</script>

<style scoped>
.projects-container{
    margin-top: 5vh;
}
.projects-title-container{
    display: flex;
    justify-content: space-between;
    align-items: center;
}
.projects-grid-container{
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 4vh 3vw;
    margin-top: 3vh;
}
</style>