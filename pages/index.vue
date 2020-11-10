<template>
  <div class="container">
    <div class="intro" @dblclick="skiptomain">
      <nav class="navbar">
        <a href="#" class="navbar-link" @click="skiptomain">Skip</a>
      </nav>
      <div class="intro-content">
        <div class="content" id="typewriter">
          <vue-typed-js
            :strings="[
              'Insipired by teachers, friends, family and the acquaintances. I am grateful. ^2000',
            ]"
            :loop="false"
            @onComplete="skiptomain"
          >
            <span class="typing"></span>
          </vue-typed-js>
        </div>
      </div>
    </div>
    <div class="container start-container">
      <div class="start-content">
        <nav class="navbar">
          <nuxt-link to="/about" class="navbar-link">About</nuxt-link>
        </nav>

        <span class="name-title">KUSHAL</span
        ><span class="name-title-a"> PATANKAR</span> <br /><br />
        <span class="subtitle">I am who I am</span>
      </div>
      <!-- <nuxt-link to="/blag" class="button">Lets Go</nuxt-link> -->
      <nuxt-link class="button" to="/blag">Lets GO</nuxt-link>
    </div>
  </div>
</template>

<script>
import JQuery from "jquery";
window.$ = JQuery;

export default {
  data() {
    return {
      introMessage: "Hello me",
    };
  },

  mounted() {
    console.log("hell");
  },
  
  methods: {
    skiptomain() {
      // $(".intro").addClass("is-fading");

      // if ($(".intro").css("opacity") == 0) {
      //   $(".intro").addClass("is-hidden");
      // }

      $(".intro").animate({opacity: 0}, 500 ,function(){$(this).fadeOut();});

      // $(".is-fading").animate({opacity:0},500,function(){
      //   $(".intro").delay(1000).addClass("is-hidden");

      // });
    },
    transition: "default",
  },
};
</script>

<style>
.button:hover {
  background-color: #f2f2f2;
  color: #0d0d0d;
}
/*
.start-content{
  text-align: center;
  background: white;
}
*/

* {
  box-sizing: border-box;
}

.button {
  position: absolute;
  bottom: 60px;
  border: 1px solid #f2f2f2;
  padding: 1em 2em;
  border-radius: 50px;
  font-size: 14px;
  color: #f2f2f2;
  text-decoration: none;
  text-transform: uppercase;
  letter-spacing: 2.002px;
  /*left: 47%;*/
  /* overflow: hidden; */
  transition: background-color 0.3s, color 0.3s;
}
/*
.button{
  position: absolute;
  font-size: 20px;
  letter-spacing: 2.002px;
  text-decoration: none;
  color: #F2F2F2;
  text-transform: uppercase;
  bottom: 60px;
  left: 50%;

}*/

vue-typed-js {
  align-content: center;
}

.subtitle {
  font-size: 20px;
  text-decoration: none;
  color: #f2f2f2;
  font-family: EB Garamond;
  font-style: italic;
  max-width: 80%;
}

.name-title {
  font-size: 80px;
  font-weight: 300;
  font-family: Montserrat;
  text-decoration: none;
  text-transform: uppercase;
  color: #f2f2f2;
}

.name-title-a {
  font-size: 80px;
  font-weight: 400;
  font-family: Montserrat;
  text-decoration: none;
  text-transform: uppercase;
  color: #f2f2f2;
}

.intro {
  margin: 0 auto;
  z-index: 100;
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  background-color: #0d0d0d;
  transition: opacity 1s;
}

.intro-content {
  width: 50%;
  max-width: 700px;
  text-align: center;
  position: absolute;
  color: #f2f2f2;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}

.content {
  font-family: EB Garamond;
  font-size: 30px;
}

.is-fading {
  opacity: 0;
}

.is-hidden {
  display: none;
}

.is-visible {
  opacity: 1;
}

.start-container {
  background-color: #0d0d0d;
  background-size: cover;
  background-position: 50%;
  margin: 0 auto;
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
}
</style>
