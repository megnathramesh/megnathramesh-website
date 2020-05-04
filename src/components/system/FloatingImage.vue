<template lang="html">
  <div>
    <div class="FloatingImage_box FloatingImage_box--color" :style="'background-color: ' + colour"></div>
    <img class="FloatingImage_box FloatingImage_box--container" v-bind:src="image" />
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
      position: absolute;

      &--color {
        float: left;
        z-index: -1;
        top: 20px;
        left: 20px;
      }

      &--container {
        z-index: -1;
      }
    }
  }
</style>
