<template lang="html">
    <div ref="bgani" class="BackgroundAnimation b-lazy">
      <div v-for="index in total" :key="index" ref="BackgroundAnimation_icon" class="BackgroundAnimation_icon"></div>
    </div>
</template>

<script lang="js">
  import { TweenLite } from 'gsap';
  import { TweenMax } from 'gsap';

  export default  {
    name: 'BackgroundAnimation',
    props: ["total"],
    mounted () {
      const container = this.$refs.bgani, w = container.clientWidth, h = container.clientHeight;
      const icons = this.$refs.BackgroundAnimation_icon;

      for (var i = 0; i < this.total; i++) {
          var icon = icons[i];
          TweenLite.set(icon, { x: this.R(0, w), y: this.R(0, h) }); // place icon 
          this.iconAnimate(icon, TweenMax);
      }
    },
    data () {
      return {
      }
    },
    methods: {
      R (min, max) { return min + (Math.floor(10 * Math.random() * (max - min)) / 10) },
      S () { return Math.random() < 0.5 ? -1 : 1 },
      Rx (deg, x) {return Math.cos(deg) * x},
      Ry (deg, y) {return Math.sin(deg) * y},
      iconAnimate (icon, tween_max) {
        // make icon rotate
        var rad = this.R(-100,100);
        var signx = Math.random() < 0.5 ? -1 : 1;
        var signy = rad < 0 ? -1 : 1;
        var rotation = (Math.asin(signy/Math.sqrt(2)) * 180 / Math.PI);
        tween_max.to(icon, 6, {
          y: '+=' + rad,
          x: '+=' + (signx * rad),
          rotationZ: rotation,
          onComplete: () => { this.iconAnimate(icon, tween_max); }
        });
      },
    },
    computed: {

    }
}


</script>

<style scoped lang="scss">
  .BackgroundAnimation {
    position: absolute;
    top: 0;
    left: 0;
    bottom: 0;
    right: 0;
    z-index: -1;
    overflow: hidden;
    pointer-events: none;

    &_icon {
        position: absolute;
        pointer-events: none;
        z-index: -1;
        width: 25px;
        height: 25px;
        background-size: contain;
        background-repeat: no-repeat;
        opacity: 0.5;

        background-image: url('../../assets/elements/rocket_emoji.png')
    }
  }
</style>
