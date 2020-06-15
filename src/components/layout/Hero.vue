<template lang="html">

  <div class="header">
    <section class="hero section">
      <div class="hero_content">
        <h1 class="app_text--title hero_text--title"> Megnath Ramesh</h1>
        <p class="hero_text--tag">Roboticist</p>
        <p class="hero_text--tag">Tech Champion</p>
        <p class="hero_text--tag">X-Factor</p>
        <p class="hero_text--intro">I love making innovative teams acheive their full potential with the relentless drive and enthusiasm I bring, along with a wide array of skills in robotics, AR/VR and IoT</p>
      </div>
    </section>
  </div>

</template>

<script lang="js">


  export default  {
    name: 'hero',
    components: { },
    props: [],
    mounted () { },
    data () { return { } },
    methods: { },
    computed: { }
}


</script>

<style scoped lang="scss">
  .header {
    background-image: url("../../assets/pics/me_1.jpg");

    height: 85vh;

    /* Create the parallax scrolling effect */
    background-attachment: fixed;
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
  }

  .hero {
    display: grid;
    grid-template-columns: 540px auto;
    grid-template-rows: 40vh;

    // Mobile layout
    @media screen and (max-width: 1000px) {
      grid-template-columns: 100%;
      grid-template-rows: auto auto;
    }

    margin-top: 0;
    padding-top: 20vh;

    &_dark {
      background: #333;
      height: 90vh;
      width: 100%;
    }

    &_content 
    { 
      justify-self: center;
      grid-row: 1;
    }

    &_text {

      &--tag {
        margin: 7px 0;
        font-size: smaller;
        color: #FFF;
      }
      &--intro { 
        margin: 30px 0;
        color: #FFF;
       }
      &--title { 
        margin: 30px 0;
        color: #FFF;
      
        &:before {
          margin: 0 0 -8px 0;
          background-image: url('../../assets/elements/rocket_emoji.png');
          background-size: cover;
          display: inline-block;
          width: 50px;
          height: 50px;
          content:"";
        }
      }
    }
  }
</style>
