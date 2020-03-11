<template lang="html">
  <div>
    <div class="FloatingImage_box FloatingImage_box--color" :style="'background-color: ' + colour"></div>
    <div class="FloatingImage_box FloatingImage_box--container">
      <div class="b-lazy image" :class="image"></div>
    </div>
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
      width: 250px;
      height: 150px;
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

  .image.abid { background-image: url("../../assets/pics/abid.jpg"); }
  .image.red { background-image: url("../../assets/pics/red.jpg"); }
  .image.sra { background-image: url("../../assets/pics/sra.jpg"); }
</style>
