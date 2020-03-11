<template lang="html">

  <section class="contact section" id="contact">
		<h1 class="app_text--title contact_title">Check Me Out</h1>
		<div class="contact_contents">
      <ButtonList class="contact_list" v-bind:list='list' />
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
    margin: 15vh auto 5vh; 

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
