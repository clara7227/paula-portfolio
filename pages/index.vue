<template>
  <div class="main">
    <div
      id="fadeIn"
      class="socials icons"
      @mouseover="hover = true"
      @mouseleave="hover = false"
    >
      <a href="https://twitter.com/miuwis/">
        <font-awesome-icon
          class="socials_item"
          :icon="{ prefix: 'fab', iconName: 'twitter' }"
      /></a>

      <a href="https://twitter.com/miuwis/"
        ><font-awesome-icon
          class="socials_item"
          :icon="{ prefix: 'fab', iconName: 'facebook' }"
      /></a>
      <a href="https://twitter.com/miuwis/">
        <font-awesome-icon class="socials_item" icon="envelope" />
      </a>
    </div>
    <div id="header" class="container">
      <Header />
    </div>
    <div class="qr"><span class="text1">CV</span></div>
    <div class="container1">
      <span class="text1" id="slideTxt">
        Hey, I’m Paula!<br />
        I’m a graphic designer and illustrator based in Madrid. I love
        classic jazz and funk, pretty landscapes, and early internet
        aesthetics.</span
      >
      <div id="fadeInHover" class="color"></div>
      <img class="illust" src="../static/2.jpg" alt="" />
    </div>
    <div class="container2">
      <span id="animate1">
        <Illust />
      </span>
    </div>
    <div class="container3">
      <span
        ><img id="fadeIn3" class="illust" src="../static/9.jpg" alt=""
      /></span>

      <div class="box" id="slideTxt1">
        <div class="text3_title">I love telling stories through my work, and conveying a sense of adventure!</div>
      </div>
    </div>
    <div class="container4">
      <span>
        <img id="fadeIn4" class="illust fix" src="../static/4.jpg" alt="" />
      </span>
      <span class="text2" id="slideTxt2">
        Freelancer with previous experience as a children's book illustrator and
        published works!
      </span>
    </div>
    <div class="container5">
      <span class="text4" id="slideTxt4">
        Clients include Manos Unidas and independent publishers.
      </span>
      <img id="fadeIn5" class="illust" src="../static/5.jpg" alt="" />
    </div>
    <div class="container6">
      <img id="fadeIn6" class="illust" src="../static/6.jpeg" alt="" />
      <span class="text5" id="slideTxt5">
        Specializes in background art and is involved in the process of
        establishing color, style, and mood of a scene.
      </span>
    </div>
    <div class="container7">
      <img id="fadeIn7" class="illust" src="../static/6.5.jpeg" alt="" />
      <span class="text6" id="slideTxt6">
        Is able to create work in a variety of styles showing strong attention to
        detail. <br> Understands architecture, has good awareness of city spaces and
        countryside landscapes.</span
      >
    </div>
    <div class="container8">
      <span
        ><img id="fadeIn8" class="illust" src="../static/8.jpg" alt="" />
      </span>
      <span>
        <img id="fadeIn9" class="illust" src="../static/7.jpg" alt="" />
      </span>
    </div>
    <div class="closer">
      <Contact />
    </div>
  </div>
</template>

<script>
import Contact from "../components/Contact.vue";
import Header from "../components/Header.vue";
import Illust from "../components/Illust.vue";

export default {
  components: { Illust, Header, Contact },
  mounted() {
    const controller = new this.$scrollmagic.Controller();

    // header

    var header = new this.$scrollmagic.Scene({
      triggerElement: ".socials",
    })
      .setTween("#header", 2, {
        scale: 1.1,
      })
      .addTo(controller);

    // CONTAINER 1

    var fadeIn = new this.$scrollmagic.Scene({
      triggerElement: ".container",
    })
      .setTween("#fadeIn", 2, {
        scale: 1.1,
      })
      .addTo(controller);

    var fadeIn2 = new this.$scrollmagic.Scene({
      triggerElement: ".container1",
    })
      .setTween("#fadeInHover", 3, {
        opacity: 0.4,
      })
      .addTo(controller);

    var slideTxt = new this.$scrollmagic.Scene({
      triggerElement: ".container1",
    })

      .setTween("#slideTxt", 3, {
        scale: 1.1,
        right: 210,
        opacity: 1,
      })
      .addTo(controller);

    // CONTAINER 2

    var slideTxt = new this.$scrollmagic.Scene({
      triggerElement: ".container3",
    })

      .setTween("#slideTxt1", 3, {
        scale: 1.1,
        right: 900,
        weight: 300,
        opacity: 1,
      })
      .addTo(controller);

    var scene = new this.$scrollmagic.Scene({ triggerElement: ".container2" })
      .setTween("#animate1", 0.5, {
        backgroundColor: "white",
        scale: 1.1,
      })
      .addTo(controller);

    // CONTAINER 3

    var fadeInHover2 = new this.$scrollmagic.Scene({
      triggerElement: ".container3",
    })
      .setTween("#fadeInHover2", 3, {
        opacity: 0.4,
      })
      .addTo(controller);

    var fadein3 = new this.$scrollmagic.Scene({
      triggerElement: ".container3",
    })
      .setTween("#fadeIn3", 2, {
        scale: 1.1,
        opacity: 1,
      })
      .addTo(controller);

    var scene2 = new this.$scrollmagic.Scene({
      triggerElement: ".container3",
      duration: 300,
    })

      .setPin("#animate2")

      .addTo(controller);

    // CONTAINER 4

    var slideTxt = new this.$scrollmagic.Scene({
      triggerElement: ".container4",
    })
      .setTween("#slideTxt2", 3, {
        scale: 1.1,
        right: 210,
        opacity: 1,
      })
      .addTo(controller);

    var slideText3 = new this.$scrollmagic.Scene({
      triggerElement: ".container4",
    })
      .setTween("#fadeIn4", 2, {
        scale: 1.1,
      })
      .addTo(controller);

    var scene3 = new this.$scrollmagic.Scene({
      triggerElement: ".container4",
      duration: 300,
    })
      .setPin("#animate3")
      .addTo(controller);

    // CONTAINER 5

    var slideTxt4 = new this.$scrollmagic.Scene({
      triggerElement: ".container5",
    })
      .setTween("#slideTxt4", 3, {
        scale: 1.1,
        right: 210,
        opacity: 1,
      })
      .addTo(controller);

    var scene4 = new this.$scrollmagic.Scene({
      triggerElement: ".container5",
      duration: 300,
    })
      .setPin("#animate3")
      .addTo(controller);

    var fadein5 = new this.$scrollmagic.Scene({
      triggerElement: ".container5",
    })
      .setTween("#fadeIn5", 2, {
        scale: 1.1,
        right: 210,
      })
      .addTo(controller);

    // CONTAINER 6

    var fadein6 = new this.$scrollmagic.Scene({
      triggerElement: ".container6",
    })
      .setTween("#fadeIn6", 2, {
        scale: 1.1,
      })
      .addTo(controller);

    var slideTxt5 = new this.$scrollmagic.Scene({
      triggerElement: ".container6",
    })
      .setTween("#slideTxt5", 3, {
        scale: 1.1,
        right: 230,
        opacity: 1,
      })
      .addTo(controller);

    // CONTAINER 7

    var slideTxt6 = new this.$scrollmagic.Scene({
      triggerElement: ".container7",
    })
      .setTween("#slideTxt6", 3, {
        scale: 1.1,
        right: 230,
        opacity: 1,
      })
      .addTo(controller);

    var fadein7 = new this.$scrollmagic.Scene({
      triggerElement: ".container7",
    })
      .setTween("#fadeIn7", 2, {
        scale: 1.1,
      })
      .addTo(controller);

    // CONTAINER 8

    var fadein8 = new this.$scrollmagic.Scene({
      triggerElement: ".container8",
    })
      .setTween("#fadeIn8, #fadeIn9", 2, {
        scale: 1.1,
      })
      .addTo(controller);
  },
};
</script>

<style lang="scss">
html,
body {
  max-width: 100%;
  overflow-x: hidden;
}

.qr {
  margin: 1rem;
}

.qr img {
  max-height: 4rem;
}

.socials {
  display: flex;
  flex-direction: row;
  position: absolute;
  margin: 1rem;
}

.socials a {
  color: #addbfc;
}

.socials a :hover {
  color: #3878a5;
}

.socials_item {
  font-style: normal;
  margin: 0.5rem;
  top: 5rem;
}

.icon {
  margin: 0.5rem;
  padding: 0;
  max-height: 1.5rem;
}

.text1 {
  position: absolute;
  max-width: 15rem;
  font-style: normal;
  font-weight: 200;
  font-size: 18px;
  line-height: 26px;
  color: #ffffff;
  right: -20rem;
  opacity: 0.5;
  z-index: 2;
}

.text2 {
  position: absolute;
  max-width: 15rem;
  font-style: normal;
  font-weight: 300;
  font-size: 18px;
  line-height: 26px;
  color: #7caed4;
  right: -20rem;
  opacity: 0.5;
  z-index: 2;
}

.text4 {
  position: absolute;
  max-width: 15rem;
  font-style: normal;
  font-weight: 300;
  font-size: 18px;
  line-height: 26px;
  color: #ffffff;
  right: -20rem;
  padding-top: 8rem;
  opacity: 0.5;
  z-index: 2;
}

.text5 {
  position: absolute;
  max-width: 15rem;
  font-style: normal;
  font-weight: 300;
  font-size: 18px;
  line-height: 26px;
  color: #7caed4;
  right: -20rem;
  padding-top: 8rem;
  opacity: 0.5;
  z-index: 2;
}

.text6 {
  position: absolute;
  max-width: 15rem;
  font-style: normal;
  font-weight: 300;
  font-size: 18px;
  line-height: 26px;
  color: #7caed4;
  right: -20rem;
  padding-top: 8rem;
  opacity: 0.5;
  z-index: 2;
}


.container {
  margin: 0 auto;
  overflow: hidden;
  min-height: 50vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.closer {
  margin: 0 auto;
  overflow: hidden;
  min-height: 50vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.container1 {
  margin: 0;
  max-width: 100%;
  min-height: 50vh;
  max-height: 5rem;
  display: flex;
  overflow: hidden;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.color {
  position: absolute;
  min-height: 50vh;
  max-height: 5rem;
  opacity: 0;
  z-index: 1;
  width: 100%;
  background: #284f75;
  background-blend-mode: multiply;
}

.container2 {
  margin: 0 auto;
  min-height: 100vh;
  max-height: 10rem;
  display: flex;
  justify-content: center;
  overflow: hidden;
  align-items: center;
  text-align: center;
  background: salmon;
}

.box {
  position: absolute;
  display: flex;
  justify-content: center;
  flex-direction: column;
  padding: 1rem;
  right: -20rem;
  opacity: 1;


}

.fix{
  display: flex;
  align-items: flex-end;
}

.text3_title {
  max-width: 14rem;
  font-style: normal;
  font-weight: 400;
  font-size: 18px;
  line-height: 26px;
  color: #ffffff;
  opacity: 1;
  z-index: 2;
}

.text3_year {
  max-width: 15rem;
  font-style: normal;
  font-weight: 300;
  font-size: 18px;
  line-height: 26px;
  color: #ffffff;

  opacity: 1;
  z-index: 2;
}

.container3 {
  margin: 0 auto;
  overflow: hidden;
  max-height: 10rem;
  width: 100%;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.container4 {
  margin: 0;
  overflow: hidden;
  max-height: 10rem;
  min-height: 100vh;
  width: 50%;
  display: flex;
  align-items: center;
  text-align: center;
}

.container5 {
  margin: 0 auto;
  overflow: hidden;
  max-height: 40rem;
  width: 100%;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: top;
  text-align: center;
}

.container5 img {
  height: 200%;
}

.container6 {
  margin: 0;
  overflow: hidden;
  max-height: 10rem;
  min-height: 100vh;
  width: 50%;
  display: flex;
  align-items: center;
  text-align: center;
}

.container7 {
  margin: 0;
  overflow: hidden;
  max-height: 10rem;
  min-height: 100vh;
  width: 50%;
  display: flex;
  align-items: center;
  text-align: center;
}

.container8 {
  margin: 0;
  overflow: hidden;
  max-height: 100rem;
  width: 100%;
  display: flex;
}

.title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont,
    "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
