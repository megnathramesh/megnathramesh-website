<template lang="html">
  <a class="button" :href="link" :title="text" :target="newTab ? 'blank' : ''">{{text}}</a>
</template>

<script lang="js">

  export default  {
    name: 'src-components-system-button',
    props: ['link', 'text', 'new-tab'],
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
    background: var(--brand-colour);
    color: var(--brand-contrastlight);
    font: var(--button-text);
    text-transform: uppercase;
    letter-spacing: 1.2px;
    line-height: 17px;
    padding: 1rem 2rem;
    position: relative;
    margin: 20px 0;
    border-radius: 3px;
    text-decoration: none;
  }
</style>
