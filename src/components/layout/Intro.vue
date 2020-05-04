<template lang="html">

  <section class="intro section" id="intro">
		<h1 class="app_text--title intro_text--title intro_item title">My Work</h1>
    <div class="intro_proj">
      <FloatingImage :image="scopear.image" :colour="scopear.colour" class="intro_item intro_item--right scopear img" />
      <div class="intro_item intro_item--left text">
        <h1 class="intro_subtitle">{{scopear.title}}</h1>
        <p class="intro_description">{{scopear.description}}</p>
        <Button class="intro_button intro_button--scopear" :new-tab="true" :link="scopear.resumebuttonlink" :text="scopear.resumebuttontext" :colour="scopear.colour" />
      </div>
    </div>
    <div class="intro_proj intro_proj--inverse">
      <div class="intro_item intro_item--right text">
        <h1 class="intro_subtitle">{{rovr_the_explorer.title}}</h1>
        <p class="intro_description">{{rovr_the_explorer.description}}</p>
        <Button class="intro_button intro_button--rovr_the_explorer" :new-tab="true" :link="rovr_the_explorer.githubbuttonlink" :text="rovr_the_explorer.githubbuttontext" :colour="rovr_the_explorer.colour" />
        <Button class="intro_button intro_button--rovr_the_explorer" :new-tab="true" :link="rovr_the_explorer.resumebuttonlink" :text="rovr_the_explorer.resumebuttontext" :colour="rovr_the_explorer.colour" />
      </div>
      <FloatingImage :image="rovr_the_explorer.image" :colour="rovr_the_explorer.colour" class="intro_item intro_item--left rovr_the_explorer img" />
    </div>
    <div class="intro_proj">
      <FloatingImage :image="paulie_blart.image" :colour="paulie_blart.colour" class="intro_item intro_item--right paulie_blart img" />
      <div class="intro_item intro_item--left text">
        <h1 class="intro_subtitle">{{paulie_blart.title}}</h1>
        <p class="intro_description">{{paulie_blart.description}}</p>
        <Button class="intro_button intro_button--paulie_blart" :new-tab="true" :link="paulie_blart.githubbuttonlink" :text="paulie_blart.githubbuttontext" :colour="paulie_blart.colour" />
        <Button class="intro_button intro_button--paulie_blart" :new-tab="true" :link="paulie_blart.resumebuttonlink" :text="paulie_blart.resumebuttontext" :colour="paulie_blart.colour" />
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
        scopear: {
          title: "Software Developer at ScopeAR",
          description: "This is what I currently do! I work with an awesome team of developers where we build an AR enabled work assistance application. We help rocket engineers train faster and get remote help at their fingertips",
          resumebuttonlink: "https://drive.google.com/file/d/1Xui-6thG-UhKMMHeErZQCkJtZO2SZ4cG/view",
          resumebuttontext: "More on Resume",
          image: require("../../assets/pics/scope_gang.jpg"),
          colour: "#2F80ED"
        },
        rovr_the_explorer: {
          title: "RoVR the Explorer",
          description: "Ever imagined how to build a real-time VR controlled robot? I tried to actually build it in a 24 hour hackathon. I was part of a team of 3, and we built a VR controlled rover with the VR headset receiving point cloud data that the robot was currently interpreting. Our project landed the 3rd place in HackED 2019, Alberta’s largest student hackathon with around 400 participants.",
          githubbuttonlink: "https://github.com/megalphian/RoVR-the-Explorer",
          githubbuttontext: "View on Github",
          resumebuttonlink: "https://drive.google.com/file/d/1Xui-6thG-UhKMMHeErZQCkJtZO2SZ4cG/view?usp=sharing",
          resumebuttontext: "More on Resume",
          image: require("../../assets/pics/me_1.jpg"),
          colour: "#EB5757"
        },
        paulie_blart: {
          title: "Paulie Blart",
          description: "This was certainly my most memorable project. I travelled to San Francisco for SFHacks 2018 and got a taste of what the tech capital of the world was like. I assembled a team with 3 other awesome student developers at the hackathon, and built an autonomous security robot with facial recognition and text controls. We called it Paulie Blart, a play on Paul Blart: Mall Cop. Paulie went on to win the 1st place in the hackathon and a bunch of other prizes!",
          githubbuttonlink: "https://github.com/megalphian/PaulieBlart",
          githubbuttontext: "View on Github",
          resumebuttonlink: "https://drive.google.com/file/d/1Xui-6thG-UhKMMHeErZQCkJtZO2SZ4cG/view?usp=sharing",
          resumebuttontext: "More on Resume",
          image: require("../../assets/pics/paulie_blart.jpg"),
          colour: "#27AE60"
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
      margin-top: calc(25vh - 50px);
      // @media screen and (max-width: 40em) {
      //   padding: 100px 7.5% 0px;
      //   display: block;
      // }

      &_proj {
        margin: 15vh auto;
        display: grid; 
        grid-template-columns: 55% auto;
        grid-template-rows: 100%;
        grid-column-gap: 10%;

        &--inverse {
          grid-template-columns: 35% auto;
        }
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
          justify-self: flex-start;
          align-self: flex-start;
          position: relative;
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
