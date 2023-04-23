<template>
  <div class="content-container">
    <Header/>
    <Introduction/>
    <Skills/>

    <img class="app-circle-img" src="@/assets/circle.svg" alt="">
  </div>
</template>

<script>
import Introduction from './components/Introduction.vue';
import Header from './components/Header.vue';
import Skills from './components/Skills.vue';

export default {
  name: 'App',
  components: {
    Introduction,
    Header,
    Skills
  }
}
</script>

<style>
body{
  background: #151515;
  margin: 0;
  color: white;
  font-size: 1vw;
  padding: 0 10vw;
}
h1{
  font-family: 'Space Grotesk';
  margin: 0;
  font-size: 4em;
}
h3{
  font-family: 'Space Grotesk';
  margin: 0;
  font-size: 3em;
}
h6{
  font-family: 'Space Grotesk';
  margin: 0;
  font-size: 2em;
  
}
p{
  font-family: 'Space Grotesk';
  margin: 0;
  font-size: 1.3em;
}
.app-circle-img{
  position: absolute;
  left: 0;
  top: 10vh;
  width: 25em;
}
</style>
