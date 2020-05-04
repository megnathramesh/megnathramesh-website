<template>
  <div id="app">
    <Hero />
    <Intro />
    <Contact />
  </div>
</template>

<script>

import Hero from './components/layout/Hero.vue'
import Intro from './components/layout/Intro.vue'
import Contact from './components/layout/Contact.vue'

export default {
  name: 'App',
  components: {
    Hero,
    Intro,
    Contact,
  }
}
</script>

<style lang="scss">

  @font-face {
    font-family: 'Rambla'; 
    src: url('./assets/fonts/Rambla-BoldItalic.ttf'); 
  }

  @font-face {
    font-family: 'Merriweather'; 
    src: url('./assets/fonts/Merriweather-Regular.ttf'); 
  }

  :root {
    --brand-colour: #12A962;
    --brand-contrastlight: white;
    --brand-contrastdark: #2c3e50;

    --brand-text: normal 20px/1.5 'Merriweather';
    --title-text: normal 50px 'Rambla';
    --subtitle-text: bold 20px/1.0 'Merriweather';
    --button-text: normal 18px 'Merriweather';
    --icon-text: normal 70px/1.3 'Merriweather';
  }

  #app {
    font: var(--brand-text);
    color: var(--brand-contrastdark);
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
  }

  .app_text--title { font: var(--title-text);  text-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25); }

  .section {
    width: 75%;
    margin: 25vh auto 15vh;
    @media screen and (max-width: 40em) { width: 85%; }
  }

  .image {
    background: linear-gradient(135deg, #dedede 0%, #dedede 40%, #bfbfbf 100%);
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;
    height: 100%;
  }
</style>
