<template lang="html">
  <div>
    <a class="button" :href="link" :title="text"  :style="'background-color: ' + colour" :target="newTab ? 'blank' : ''">
      {{text}}
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
    display: block;

    &:after {
      margin: 0 0 -8px 0;
      background-image: url('../../assets/elements/rocket_emoji.png');
      background-size: cover;
      width: 30px;
      height: 30px;
      content:"";
      position: absolute;
      top: 30px;
      right: -12px;
    } 
  }
</style>
