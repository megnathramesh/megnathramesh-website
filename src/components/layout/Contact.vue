<template lang="html">

  <section class="contact section" id="contact">
    <BackgroundAnimation class="contact_bgani" :total='number_of_rockets' />
		
    <h1 class="app_text--title contact_title">Check Me Out</h1>
		<div class="contact_contents">
      <ButtonList class="contact_list" v-bind:list='list' />
		</div>
  </section>

</template>

<script lang="js">
  import ButtonList from './../system/ButtonList.vue'
  import BackgroundAnimation from './../system/BackgroundAnimation.vue'

  export default  {
    name: 'contact',
    components: {
      ButtonList,
      BackgroundAnimation
    },
    props: [],
    mounted () {

    },
    data () {

      var width = window.innerWidth;
      var no_rockets = width <= 600 ? 14 : 25;
      console.log(no_rockets);
      return {
        number_of_rockets: no_rockets,
        list: [
          {link: "https://github.com/megalphian",           icon: "github"},
          {link: "https://twitter.com/MegnathR",            icon: "twitter"},
          {link: "https://linkedin.com/in/megnath-ramesh",  icon: "linkedin"},
          {link: "mailto:megnath.ramesh@gmail.com",           icon: "envelope"},
        ]
      }
    },
    methods: {

    },
    computed: {

    }
}


</script>

<style scoped lang="scss">
  .contact {
    position: relative;
    margin: 25vh auto 8vh; 
      
    &_bgani {
      background-color: rgba(161, 161, 161, 0.24);  
      backdrop-filter: blur(5px);

      @media screen and (max-width: 581px) {
        bottom: -8vh;
        top: -3vh;
        left: -8vw;
        right: -8vw;
      }
      
      @media screen and (min-width: 581px) {
        left: -15vw;
        bottom: -8vh;
        right: -15vw;
        top: -3vh;
      }
    }

    &_title { margin: 0; }

    &_contents {
      padding: 10vh 0;
      width: 100%;
      margin: auto;
      display: grid;
      grid-template-columns: auto;
      grid-template-rows: auto auto;
      grid-row-gap: 2.5vh;
    }

    &_list {
      grid-column-start: 1;
      grid-column-end: 1;
      grid-row-start: 2;
      grid-row-end: 3;
      position: relative;
      margin: auto;
    }
  }
</style>
