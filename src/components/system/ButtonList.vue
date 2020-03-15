<template lang="html">
  <ul class="buttonlist">
    <li v-for="item in list" :key="item.icon" class="icon">
      <a :href="item.link" class="buttonlist_icon">
        <font-awesome-icon :icon="icon[item.icon]" />
      </a>
    </li>
  </ul>
</template>

<script lang="js">
  import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome'
  import { faEnvelope, faEdit } from '@fortawesome/free-regular-svg-icons'
  import { faTwitter, faGithub, faLinkedinIn, faCodepen } from '@fortawesome/free-brands-svg-icons'

  export default  {
    name: 'ButtonList',
    components: {
      FontAwesomeIcon
    },
    props: ['hasButton', 'button', 'list'],
    mounted () {

    },
    data () {
      return {
        icon: {
          envelope: faEnvelope,
          edit: faEdit,
          twitter: faTwitter,
          github: faGithub,
          linkedin: faLinkedinIn,
          codepen: faCodepen,
        }
      }
    },
    methods: {

    },
    computed: {

    }
  }

</script>

<style scoped lang="scss">
  .buttonlist {
    position: absolute;
    padding-left: 0px;
  
    li {
      float: left;
      list-style: none;
      &:not(:first-of-type) { margin: 0 0 0 40px; }

      a.buttonlist_icon {
        font: var(--icon-text);
        color: var(--brand-contrastdark);
      }
    }
  }
</style>
