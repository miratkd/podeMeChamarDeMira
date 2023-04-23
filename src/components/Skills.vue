<template>
    <div>
        <div class="skills-row">
            <div class="skill-cell">
                <h1>HTML/CSS</h1>
                <p>2 anos de experiência</p>
            </div>
            <div class="skill-cell">
                <h1>Javascript</h1>
                <p>2 anos de experiência</p></div>
            <div class="skill-cell">
                <h1>Vue.JS</h1>
                <p>2 anos de experiência</p></div>
        </div>
        <div class="skills-row">
            <div class="skill-cell">
                <h1>Python</h1>
                <p>1 ano de experiência</p>
            </div>
            <div class="skill-cell">
                <h1>Django Rest</h1>
                <p>1 ano de experiência</p>
            </div>
            <div class="skill-cell">
                <h1>SQL/Postgresql</h1>
                <p>1 ano de experiência</p>
            </div>
        </div>
        <div class="skills-row">
            <div class="skill-cell">
                <h1>Agile</h1>
                <p>2 anos de experiência</p>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'SkillsComponent'
}
</script>

<style scoped>
.skills-row{
    display: flex;
    margin-top: 5vh;
}
.skill-cell{
    width: 33%;
}
</style>