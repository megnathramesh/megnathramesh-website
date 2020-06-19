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
          this.iconRotate(icon, TweenMax);
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
      iconRotate (icon, tween_max) {
        // make icon rotate
        var rad = this.R(0,1) * 120;
        var rotation = Math.random(0,1) * 360;
        var angleWithOffsetInRadians = ((rotation - 45) % 360) * (Math.PI / 180) ;
        var x = 2*(Math.cos(angleWithOffsetInRadians)  * rad);
        var y = 2*(Math.sin(angleWithOffsetInRadians) * rad);
        
        tween_max.to(icon, {
          rotationZ: rotation,
          duration: this.R(1, 3),
          onComplete: () => { this.iconMove(icon, tween_max, x, y); }
        });
      },
      iconMove (icon, tween_max, x, y) {
        tween_max.to(icon, {
          y: '+=' + y,
          x: '+=' + x,
          ease: "power3.out",
          duration: this.R(1, 3),
          onComplete: () => { this.iconRotate(icon, tween_max); }
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
