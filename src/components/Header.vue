<template>
    <div class="header-container">
        <p class="header-name-text">LucasMira</p>
        <div class="header-icons-container">
            <img v-if="!languagePortuguese" @click="updateLanguage" class="header-ptbr-icon" src="@/assets/pt-br.avif" title="Trocar texto para Português" alt="Trocar texto para Português">
            <img v-else class="header-ptbr-icon" @click="updateLanguage" src="@/assets/usaicon.jpeg" title="Change text to English" alt="Change text to English">
            <a href="https://www.codewars.com/users/miratkd" target="_blank">
                <img class="header-icon" src="@/assets/codeWars.png" alt="CodeWars">
            </a>
            <a href="https://github.com/miratkd" target="_blank">
                <img class="header-icon" src="@/assets/github.svg" alt="GitHub">
            </a>
            <a href="https://www.linkedin.com/in/lucas-mira-17514b203/" target="_blank">
                <img class="header-icon" src="@/assets/LinkedIn.svg" alt="LinkId">
            </a>
        </div>
    </div>
</template>

<script>
export default {
    name: 'HeaderComponet',
    props:['languagePortuguese', 'updateLanguage']
}
</script>

<style scoped>
.header-container {
    position: absolute;
    z-index: 2;
    height: 10vh;
    width: 80vw;
    display: flex;
    align-items: center;
    justify-content: space-between;
}

.header-name-text {
    font-weight: 700;
    font-size: 2.3em;
}

.header-icons-container {
    display: flex;
    gap: 2em;
    margin-right: 3vw;
    align-items: center;
}

.header-icon {
    width: 2.5em;
    cursor: pointer;
}

.header-ptbr-icon {
    height: 3vh;
    cursor: pointer;
    border-radius: 10px;
}

@media screen and (max-width: 850px) {
    .header-container {
        width: 90%;
        padding: 0 5%
    }

    .header-icons-container {
        margin-right: 0;
    }
}

@media screen and (max-width: 450px) {
    .header-container {
        flex-direction: column;
        justify-content: center;
        gap: 15%;
    }
}
</style>