<template>
    <div>
        <div class="skills-row">
            <div class="skill-cell">
                <h3>HTML/CSS</h3>
                <p>2 anos de experiência</p>
            </div>
            <div class="skill-cell">
                <h3>Javascript</h3>
                <p>2 anos de experiência</p></div>
            <div class="skill-cell">
                <h3>Vue.JS</h3>
                <p>2 anos de experiência</p></div>
        </div>
        <div class="skills-row">
            <div class="skill-cell">
                <h3>Python</h3>
                <p>1 ano de experiência</p>
            </div>
            <div class="skill-cell">
                <h3>Django Rest</h3>
                <p>1 ano de experiência</p>
            </div>
            <div class="skill-cell">
                <h3>SQL/Postgresql</h3>
                <p>1 ano de experiência</p>
            </div>
        </div>
        <div class="skills-row">
            <div class="skill-cell">
                <h3>Agile</h3>
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