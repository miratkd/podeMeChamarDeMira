<template>
    <div class="skills-container">
        <div class="skills-row">
            <div class="skill-cell">
                <h3>HTML/CSS</h3>
                <p>4 {{ languagePortuguese ? 'anos de experiência' : 'Years of experience' }}</p>
            </div>
            <div class="skill-cell">
                <h3>JavaScript/TypeScript</h3>
                <p>4 {{ languagePortuguese ? 'anos de experiência' : 'Years of experience' }}</p></div>
            <div class="skill-cell">
                <h3>Vue.JS</h3>
                <p>4 {{ languagePortuguese ? 'anos de experiência' : 'Years of experience' }}</p></div>
        </div>
        <div class="skills-row">
            <div class="skill-cell">
                <h3>PHP</h3>
                <p>2 {{ languagePortuguese ? 'anos de experiência' : 'Years of experience' }}</p>
            </div>
            <div class="skill-cell">
                <h3>Laravel Rest</h3>
                <p>2 {{ languagePortuguese ? 'anos de experiência' : 'Years of experience' }}</p>
            </div>
            <div class="skill-cell">
                <h3>Python</h3>
                <p>1 {{ languagePortuguese ? 'ano de experiência' : 'Year of experience' }}</p>
            </div>
        </div>
        <div class="skills-row">
            <div class="skill-cell">
                <h3>Django Rest</h3>
                <p>1 {{ languagePortuguese ? 'ano de experiência' : 'Year of experience' }}</p>
            </div>
            <div class="skill-cell">
                <h3>SQL/Postgresql</h3>
                <p>1 {{ languagePortuguese ? 'ano de experiência' : 'Year of experience' }}</p>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'SkillsComponent',
    props:['languagePortuguese'],
}
</script>

<style scoped>
.skills-row{
    display: flex;
    margin-top: 5vh;
}
.skill-cell{
    width: 33%;
    text-align: center;
}
.skills-container{
    border-top: 1px solid white;
}
@media screen and (max-width: 850px){
    .skills-container{
        margin: 0 3vw;
    }
}
@media screen and (max-width: 450px) {
    .skills-row{
        flex-direction: column;
        align-items: center;
        text-align: center;
        margin-top: 0;
    }
    .skills-container{
        padding-top: 5vh;
    }
    .skill-cell{
        width: 100%;
        margin-bottom: 2.5vh;
    }
}
</style>