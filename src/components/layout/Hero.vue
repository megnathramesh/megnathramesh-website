<template lang="html">

  <section class="hero section">
		<h1 class="hero_text--title">Megnath Ramesh</h1>
		<p class="hero_text--tag">Tech Champion</p>
		<p class="hero_text--tag">Roboticist</p>
		<p class="hero_text--tag">X-Factor</p>
		<p class="hero_text--intro">I love making innovative teams acheive their full potential with the relentless drive and enthusiasm I bring, along with a wide array of skills in robotics, AR/VR and IOT</p>
  </section>

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
    > * {
      width: 50%;
      @media screen and (max-width: 40em) { width: unset; }
    }

    &_nameImg { width: 200px; }

    &_text--tag {
      margin-top: 7px;
      margin-bottom: 30px;
    }
  }
</style>
