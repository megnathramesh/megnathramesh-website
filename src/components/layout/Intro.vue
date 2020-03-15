<template lang="html">

  <section class="intro section" id="intro">
		<h1 class="app_text--title intro_text--title intro_item title">My Work</h1>
    <div class="intro_proj">
      <FloatingImage :image="blart.image" :colour="blart.colour" class="intro_item intro_item--right blart img" />
      <div class="intro_item intro_item--left blart text">
        <h1 class="intro_subtitle">{{blart.title}}</h1>
        <p class="intro_description">{{blart.description}}</p>
        <Button class="intro_button intro_button--blart" :link="blart.buttonlink" :text="blart.buttontext" :colour="blart.colour" />
      </div>
    </div>
    <div class="intro_proj">
      <FloatingImage :image="ROS.image" :colour="ROS.colour" class="intro_item intro_item--left ROS img" />
      <div class="intro_item intro_item--right ROS text">
        <h1 class="intro_subtitle">{{ROS.title}}</h1>
        <p class="intro_description">{{ROS.description}}</p>
        <Button class="intro_button intro_button--ROS" :link="ROS.buttonlink" :text="ROS.buttontext" :colour="ROS.colour" />
      </div>
    </div>
    <div class="intro_proj">
      <FloatingImage :image="RL.image" :colour="RL.colour" class="intro_item intro_item--right RL img" />
      <div class="intro_item intro_item--left RL text">
        <h1 class="intro_subtitle">{{RL.title}}</h1>
        <p class="intro_description">{{RL.description}}</p>
        <Button class="intro_button intro_button--RL" :link="RL.buttonlink" :text="RL.buttontext" :colour="RL.colour" />
      </div>
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
          image: "../../assets/img/blart.png",
          colour: "#2F80ED"
        },
        ROS: {
          title: "ROS => Rover️ Projects",
          description: "I do a lot of really cool stuff, basically yeah it’s really cool",
          buttonlink: "https://github.com/megalphian/PaulieBlart",
          buttontext: "View on Github",
          image: "../../assets/img/ROS.png",
          colour: "#27AE60"
        },
        RL: {
          title: "RL Certification",
          description: "I do a lot of really cool stuff, basically yeah it’s really cool",
          buttonlink: "https://github.com/megalphian/PaulieBlart",
          buttontext: "View on Github",
          image: "../../assets/img/RL.png",
          colour: "#EB5757"
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
      // @media screen and (max-width: 40em) {
      //   padding: 100px 7.5% 0px;
      //   display: block;
      // }

      &_proj {
        width: 90%;
        margin: 15vh auto;
        display: grid; 
        grid-template-columns: 45% auto;
        grid-template-rows: 100%;
        grid-column-gap: 10%;
      }

      &_item {
        &--left {
          grid-column-start: 1;
          grid-column-end: 2;
          grid-row: 1;
        }

        &--right {
          grid-column-start: 2;
          grid-column-end: 3;
          grid-row: 1;
        }

        &.img {
          justify-self: center;
          align-self: center;
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
