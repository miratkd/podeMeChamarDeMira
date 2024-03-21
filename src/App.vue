<template>
  <div>
    <div class="content-container">
      <Header />
      <Introduction :languagePortuguese="languagePortuguese"/>
      <Skills :languagePortuguese="languagePortuguese"/>
      <Projects :languagePortuguese="languagePortuguese"/>
    </div>
    <Footer />

    <!-- absolute -->
      <img class="app-circle-img" src="@/assets/circle.svg" alt="">
      <img class="app-circle-img-2" src="@/assets/circle2.svg" alt="">
  </div>
</template>

<script>
import Introduction from './components/Introduction.vue';
import Header from './components/Header.vue';
import Skills from './components/Skills.vue';
import Projects from './components/Projects.vue';
import Footer from './components/Footer.vue';

export default {
  name: 'App',
  components: {
    Introduction,
    Header,
    Skills,
    Projects,
    Footer
  },
  data(){
    return{
      languagePortuguese: (navigator.language || navigator.userLanguage) == 'pt-BR'
    }
  }
}
</script>

<style>
body {
  background: #151515;
  margin: 0;
  color: white;
  font-size: 1vw;
  
}
.content-container{
  padding: 0 10vw;
}

h1 {
  font-family: 'Space Grotesk';
  margin: 0;
  font-size: 4em;
}

h3 {
  font-family: 'Space Grotesk';
  margin: 0;
  font-size: 3em;
}

h6 {
  font-family: 'Space Grotesk';
  margin: 0;
  font-size: 2em;

}

p {
  font-family: 'Space Grotesk';
  margin: 0;
  font-size: 1.3em;
}

.app-circle-img {
  position: absolute;
  left: 0;
  top: 10vh;
  width: 25em;
}

.app-circle-img-2 {
  position: absolute;
  right: 0;
  top: 110vh;
  width: 18em;
}
@media screen and (max-width: 850px) {
  body{
    font-size: 1.5vw;
  }
  .content-container{
    padding: 0;
  }
  .app-circle-img{
    width: 20em;
    top: 8vh;
  }
  .app-circle-img-2 {
    top: 70vh;
  }
}
@media screen and (max-width: 450px) {
  .app-circle-img {
    top: 20vh;
    width: 22em;
    left: -20%;
  }
  body{
    font-size: 2.5vw;
  }
  h1 {
    font-size: 3em;
  }
  .app-circle-img-2 {
    top: 110vh;
    width: 12em;
  }
  p {
    font-size: 1.5em;
  }
}
</style>
