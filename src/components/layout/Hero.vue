<template lang="html">

  <div class="header">
    <section class="hero section">
      <div class="hero_content">
        <h1 class="app_text--title hero_text--title"> Megnath Ramesh</h1>
        <ButtonList class="contact_list" v-bind:list='list' />
        <p class="hero_text--tag">Roboticist</p>
        <p class="hero_text--tag">Tech Champion</p>
        <p class="hero_text--tag">X-Factor</p>
        <p class="hero_text--intro">I love making innovative teams acheive their full potential with the relentless drive and enthusiasm I bring, along with a wide array of skills in robotics, AR/VR and IoT</p>
      </div>
    </section>
  </div>

</template>

<script lang="js">
  import ButtonList from './../system/ButtonList.vue'

  export default  {
    name: 'hero',
    components: {
      ButtonList
     },
    props: [],
    mounted () { },
    data () { 
      return {
        list: [
          {link: "https://github.com/megalphian",           icon: "github"},
          {link: "https://twitter.com/MegnathR",            icon: "twitter"},
          {link: "https://linkedin.com/in/megnath-ramesh",  icon: "linkedin"},
          {link: "mailto:megnath.ramesh@gmail.com",           icon: "envelope"},
        ]
      } 
     },
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

    @media screen and (min-width: 950px) {
      /* Create the parallax scrolling effect */
      background-attachment: fixed;
    }

    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
  }

  .hero {
    display: grid;
    margin-top: 20vh;
    margin-bottom: 2vh;
    grid-template-columns: minmax(240px, 540px);
    grid-template-rows: minmax(min-content, max-content);

    // Mobile layout
    @media screen and (max-width: 950px) {
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
        margin-bottom: 0;
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

  .contact {
    &_contents {
      grid-column: 2;
    }
    &_list {
      grid-column-start: 1;
      grid-column-end: 1;
      grid-row-start: 2;
      grid-row-end: 3;
      position: relative;
      margin: 7px 0;
      font-size: smaller;
    }
  }
</style>
