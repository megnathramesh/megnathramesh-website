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
    <div class="scroll">
      <img class="scroll_icon" src="../../assets/elements/arrow_down.png"/>
    </div>
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
    background-image: 
    linear-gradient(
      rgba(0.5, 0.5, 0.5, 0.15),
      rgba(0, 0, 0, 0.75)
    ),
    url("../../assets/pics/me_1.jpg");

    display: grid;
    min-height: 100vh;

    @supports not (-webkit-touch-callout: none) {
      /* Create the parallax scrolling effect */
      background-attachment: fixed;
    }

    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
  }

  .hero {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(240px, 540px));
    grid-template-rows: repeat(auto-fit, minmax(min-content, max-content));
    margin-top: 20vh;
    margin-bottom: 2vh;

    // Mobile layout
    @media screen and (max-width: 600px)  {
      grid-template-columns: 100%;
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

  .scroll {
    display: grid;
    margin-left: auto;
    margin-right: auto;
    grid-template-rows: repeat(auto-fit, minmax(min-content, max-content));
    align-items: center;

    &_icon {
      max-width:150px;
      max-height:150px;
      width: auto;
      height: auto;
      filter: contrast(15%);
      opacity: 0.65;
    }
  }
</style>
