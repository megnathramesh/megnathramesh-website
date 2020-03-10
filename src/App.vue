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

  :root {
    --brand-colour: #12A962;
    --brand-contrastlight: white;
    --brand-contrastdark: #2c3e50;

    --brand-text: normal 18px/1.3 'Lato';
    --button-text: normal 700 15px 'Raleway';
    --icon-text: normal 18px/1.3 'Lato';
  }

  #app {
    font: var(--brand-text);
    color: var(--brand-contrastdark);
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
  }

  .section {
    width: 70%;
    margin: 25vh auto 15vh;
    @media screen and (max-width: 40em) { width: 85%; }
  }

  .image {
    background: linear-gradient(135deg, #dedede 0%, #dedede 40%, #bfbfbf 100%);
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;
    height: 100%;
    border-radius: 3px;
  }

  .portfolio_item--title,
  .text.big,
  .contact_contents--title {
    font-family: 'raleway';
    font-weight: 700;
    font-size: 30px;
  }

</style>
