<template lang="html">

  <section class="contact contact-style b-loaded" id="contact">
		<h1 class="intro_text--title">Check Me Out</h1>
		<div class="contact_contents">
      <ButtonList class="contact_contents--links" :hasButton=false v-bind:list='list' />
		</div>
  </section>

</template>

<script lang="js">
  import ButtonList from './../system/ButtonList.vue'

  export default  {
    name: 'contact',
    components: {
      ButtonList,
    },
    props: [],
    mounted () {

    },
    data () {
    return {
        list: [
          {link: "https://github.com/megalphian",           icon: "github"},
          {link: "https://twitter.com/MegnathR",            icon: "twitter"},
          {link: "https://linkedin.com/in/megnath-ramesh",  icon: "linkedin"},
          // {link: "mailto:megnath@ualberta.ca",           icon: "envelope"},
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
    z-index: 1;
    text-align: center;
    width: 100%;
    position: relative;
    bottom: 0;
    margin: 0;
    min-height: 400px;

    &_contents {
      padding: 10vh 0;
      width: 100%;
      margin: auto;
      display: grid;
      grid-template-columns: auto;
      grid-template-rows: auto auto;
      grid-row-gap: 2.5vh;

      &--title {
        color: #ffffff;
        margin: 20px 0 0 0;
        grid-column-start: 1;
        grid-column-end: 1;
        grid-row-start: 1;
        grid-row-end: 2;
      }

      &--links {
        grid-column-start: 1;
        grid-column-end: 1;
        grid-row-start: 2;
        grid-row-end: 3;
        position: relative;
        margin: auto;
      }
    }
  }
</style>
