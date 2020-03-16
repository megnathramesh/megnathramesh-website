<template lang="html">
  <a class="button" :href="link" :title="text"  :style="'background-color: ' + colour" :target="newTab ? 'blank' : ''">{{text}}</a>
</template>

<script lang="js">

  export default  {
    name: 'src-components-system-button',
    props: ['link', 'text', 'new-tab', 'colour'],
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
  .button {
    color: var(--brand-contrastlight);
    font: var(--button-text);
    padding: 1rem 2rem;
    text-decoration: none;
    
    margin-right: 20px;
  }
</style>
