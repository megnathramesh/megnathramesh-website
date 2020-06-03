<template lang="html">
  <div>
    <a class="button" :href="link" :title="text"  :style="'background-color: ' + colour" :target="newTab ? 'blank' : ''">
      {{text}}
      <img class="rocket" src="../../assets/elements/rocket_emoji.png" />
    </a>
  </div>
</template>

<script lang="js">

  export default  {
    name: 'src-components-system-button',
    props: ['link', 'text', 'new-tab', 'colour'],
    mounted () { },
    data () { return { } },
    methods: { },
    computed: { }
}


</script>

<style scoped lang="scss">
  .button {
    color: var(--brand-contrastlight);
    font: var(--button-text);
    padding: 1rem 2rem;
    text-decoration: none;
    
    margin-right: 20px;
    position: relative;
  }

  .rocket {
    width: 30px;
    position: absolute;
    top: 30px;
    right: -12px;
  }
</style>
