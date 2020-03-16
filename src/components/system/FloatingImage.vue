<template lang="html">
  <div>
    <div class="FloatingImage_box FloatingImage_box--color" :style="'background-color: ' + colour"></div>
    <img class="FloatingImage_box FloatingImage_box--container image" v-bind:src="image" />
  </div>
</template>

<script lang="js">

  export default  {
    name: 'FloatingImage',
    props: ["image", "colour"],
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

<style lang="scss">

  .FloatingImage {
    &_box {
      width: 300px;
      height: 200px;
      position: relative;

      &--color {
        float: left;
        z-index: -1;
      }

      &--container {
        z-index: -1;
        background-size: cover;
        background-color: transparent;
        background-repeat: no-repeat;
        background-position: 50% 50%;
        background-image: none;
        left: 20px;
        top: -20px;
      }
    }
  }
</style>
