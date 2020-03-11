<template lang="html">

  <section class="intro section" id="intro">
		<h1 class="app_text--title intro_text--title intro_item title">My Work</h1>
    <FloatingImage :image="blart.image" class="intro_item intro_item blart img" />
    <div class="intro_item blart text">
      <h1 class="intro_subtitle">{{blart.title}}</h1>
      <p class="intro_description">{{blart.description}}</p>
      <Button class="intro_button intro_button--blart" :link="blart.buttonlink" :text="blart.buttontext" />
    </div>
    <div class="intro_item ROS text">
      <h1 class="intro_subtitle">{{ROS.title}}</h1>
      <p class="intro_description">{{ROS.description}}</p>
      <Button class="intro_button intro_button--ROS" :link="ROS.buttonlink" :text="ROS.buttontext" />
    </div>
    <FloatingImage :image="ROS.image" class="intro_item intro_item ROS img" />
    <FloatingImage :image="RL.image" class="intro_item intro_item RL img" />
    <div class="intro_item RL text">
      <h1 class="intro_subtitle">{{RL.title}}</h1>
      <p class="intro_description">{{RL.description}}</p>
      <Button class="intro_button intro_button--RL" :link="RL.buttonlink" :text="RL.buttontext" />
    </div>
  </section>

</template>

<script lang="js">

  import FloatingImage from './../system/FloatingImage.vue'
  import Button from './../system/Button.vue'

  export default  {
    name: 'intro',
    components: {
      FloatingImage,
      Button,
    },
    props: [],
    mounted () {

    },
    data () {
      return {
        blart: {
          title: "Paulie Blart",
          description: "Paulie Blart is a Security Robot and won 1st place at SFHacks 2018",
          buttonlink: "https://github.com/megalphian/PaulieBlart",
          buttontext: "View on Github",
          image: "../../assets/img/blart.png"
        },
        ROS: {
          title: "ROS => Rover️ Projects",
          description: "I do a lot of really cool stuff, basically yeah it’s really cool",
          buttonlink: "https://github.com/megalphian/PaulieBlart",
          buttontext: "View on Github",
          image: "../../assets/img/ROS.png"
        },
        RL: {
          title: "RL Certification",
          description: "I do a lot of really cool stuff, basically yeah it’s really cool",
          buttonlink: "https://github.com/megalphian/PaulieBlart",
          buttontext: "View on Github",
          image: "../../assets/img/RL.png"
        },
      }
    },
    methods: {

    },
    computed: {

    }
}


</script>

<style scoped lang="scss">
  .intro {
      position: relative;
      padding: 100px 0 0;
      display: grid;
      grid-template-columns: 5% 5% 5% 30% 5% 5% auto 10%;
      grid-template-rows: 10rem 2rem 19rem 5rem 18rem 2rem;
      // @media screen and (max-width: 40em) {
      //   padding: 100px 7.5% 0px;
      //   display: block;
      // }

      &_item {
        &.title {
          grid-column-start: 1;
          grid-column-end: 4;
          grid-row-start: 1;
          grid-row-end: 2;
        }

        &.blart {
          &.img {
            grid-column-start: 3;
            grid-column-end: 5;
            grid-row-start: 2;
            grid-row-end: 3;
          }
          &.text {
            grid-column-start: 5;
            grid-column-end: 8;
            grid-row-start: 3;
            grid-row-end: 4;
          }
        }

        &.ROS {
          &.img {
            grid-column-start: 7;
            grid-column-end: 8;
            grid-row-start: 5;
            grid-row-end: 6;
          }
          &.text {
            grid-column-start: 2;
            grid-column-end: 5;
            grid-row-start: 4;
            grid-row-end: 5;
          }
        }

        &.RL {
          &.img {
            grid-column-start: 4;
            grid-column-end: 4;
            grid-row-start: 6;
            grid-row-end: 7;
          }
          &.text {
            grid-column-start: 6;
            grid-column-end: 8;
            grid-row-start: 7;
            grid-row-end: 8;
          }
        }
      }

      &_subtitle {
        font: var(--subtitle-text);
      }

      &_button {
        display: inline-block;
        margin-top: 0;
      }
  }
</style>
