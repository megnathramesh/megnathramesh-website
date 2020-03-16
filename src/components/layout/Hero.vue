<template lang="html">

  <div class="hero_dark">
    <section class="hero section">
      <div class="hero_left">
        <h1 class="app_text--title hero_text--title">Megnath Ramesh</h1>
        <p class="hero_text--tag">Tech Champion</p>
        <p class="hero_text--tag">Roboticist</p>
        <p class="hero_text--tag">X-Factor</p>
        <p class="hero_text--intro">I love making innovative teams acheive their full potential with the relentless drive and enthusiasm I bring, along with a wide array of skills in robotics, AR/VR and IOT</p>
      </div>
      <div class="hero_right">
        <img class="hero_img" src="../../assets/pics/kingmeg.png" />
      </div>
    </section>
  </div>

</template>

<script lang="js">


  export default  {
    name: 'hero',
    components: {
    },
    props: [],
    mounted () {

    },
    data () {
      return {
      }
    },
    methods: {

    },
    computed: {

    }
}


</script>

<style scoped lang="scss">
  .hero {
    display: grid;
    grid-template-columns: 50% auto;
    grid-template-rows: 40vh;

    margin-top: 0;
    padding-top: 25vh;
    color: white !important;

    &_dark {
      background: #333;
      height: 90vh;
      width: 100%;
    }

    &_right { justify-self: center; }

    &_img { height: 100%; }

    &_text {
      &--tag {
        margin: 7px 0;
        font-size: smaller;
      }
      &--intro { margin: 30px 0; }
      &--title { margin: 30px 0; }
    }

  }
</style>
