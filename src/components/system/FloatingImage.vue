<template lang="html">
  <div>
    <div class="FloatingImage_box FloatingImage_box--color"></div>
    <div class="FloatingImage_box FloatingImage_box--container">
      <div class="b-lazy image" :class="image"></div>
    </div>
  </div>
</template>

<script lang="js">

  export default  {
    name: 'FloatingImage',
    props: ["image"],
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
      border-radius: 3px;
      position: relative;

      &--color {
        background: #12A962;
        float: left;
        z-index: -1;
      }

      &--container {
        box-shadow: -20px 26px 54px rgba(51, 51, 51, 0.28);
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
