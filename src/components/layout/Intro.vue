<template lang="html">

  <section class="intro section" id="intro">
		<h1 class="app_text--title intro_text--title intro_item title">My Work</h1>
    <FloatingImage :image="scopear.image" :colour="scopear.colour" class="intro_item intro_item scopear img" />
    <div class="intro_item scopear text">
      <h1 class="intro_subtitle">{{scopear.title}}</h1>
      <p class="intro_description">{{scopear.description}}</p>
      <Button class="intro_button intro_button--scopear" :link="scopear.resumebuttontext" :text="scopear.resumebuttontext" :colour="scopear.colour" />
    </div>
    <div class="intro_item rovr_the_explorer">
      <h1 class="intro_subtitle">{{rovr_the_explorer.title}}</h1>
      <p class="intro_description">{{rovr_the_explorer.description}}</p>
      <Button class="intro_button intro_button--rovr_the_explorer" :link="rovr_the_explorer.githubbuttontext" :text="rovr_the_explorer.githubbuttontext" :colour="rovr_the_explorer.colour" />
      <Button class="intro_button intro_button--rovr_the_explorer" :link="rovr_the_explorer.resumebuttontext" :text="rovr_the_explorer.resumebuttontext" :colour="rovr_the_explorer.colour" />
    </div>
    <FloatingImage :image="rovr_the_explorer.image" :colour="rovr_the_explorer.colour" class="intro_item intro_item rovr_the_explorer img" />
    <FloatingImage :image="paulie_blart.image" :colour="paulie_blart.colour" class="intro_item intro_item paulie_blart img" />
    <div class="intro_item paulie_blart text">
      <h1 class="intro_subtitle">{{paulie_blart.title}}</h1>
      <p class="intro_description">{{paulie_blart.description}}</p>
      <Button class="intro_button intro_button--paulie_blart" :link="paulie_blart.githubbuttonlink" :text="paulie_blart.githubbuttontext" :colour="paulie_blart.colour" />
      <Button class="intro_button intro_button--paulie_blart" :link="paulie_blart.resumebuttonlink" :text="paulie_blart.resumebuttontext" :colour="paulie_blart.colour" />
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
          resumebuttonlink: "https://drive.google.com/file/d/1Xui-6thG-UhKMMHeErZQCkJtZO2SZ4cG/view?usp=sharing",
          resumebuttontext: "More on Resume",
          image: "../../assets/pics/scope_gang.jpg",
          colour: "#2F80ED"
        },
        rovr_the_explorer: {
          title: "RoVR the Explorer",
          description: "Ever imagined how to build a real-time VR controlled robot? I tried to actually build it in a 24 hour hackathon. I was part of a team of 3, and we built a VR controlled rover with the VR headset receiving point cloud data that the robot was currently interpreting. Our project landed the 3rd place in HackED 2019, Alberta’s largest student hackathon with around 400 participants.",
          githubbuttonlink: "https://github.com/megalphian/RoVR-the-Explorer",
          githubbuttontext: "View on Github",
          resumebuttonlink: "https://drive.google.com/file/d/1Xui-6thG-UhKMMHeErZQCkJtZO2SZ4cG/view?usp=sharing",
          resumebuttontext: "More on Resume",
          image: "../../assets/img/RL.png",
          colour: "#EB5757"
        },
        paulie_blart: {
          title: "Paulie Blart",
          description: "This was certainly my most memorable project. I travelled to San Francisco for SFHacks 2018 and got a taste of what the tech capital of the world was like. I assembled a team with 3 other awesome student developers at the hackathon, and built an autonomous security robot with facial recognition and text controls. We called it Paulie Blart, a play on Paul Blart: Mall Cop. Paulie went on to win the 1st place in the hackathon and a bunch of other prizes!",
          githubbuttonlink: "https://github.com/megalphian/PaulieBlart",
          githubbuttontext: "View on Github",
          resumebuttonlink: "https://drive.google.com/file/d/1Xui-6thG-UhKMMHeErZQCkJtZO2SZ4cG/view?usp=sharing",
          resumebuttontext: "More on Resume",
          image: "../../assets/pics/paulie_blart.jpg",
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

        &.scopear {
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

        &.rovr_the_explorer {
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

        &.paulie_blart {
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
