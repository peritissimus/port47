<template>
  <div class="about">
      <nav class="navbar">
        <nuxt-link to="/" class="navbar-link">Home</nuxt-link>
      </nav>
      <div class="about__content">
        <span class="content">
          <span>
            Hello. You can access the public information about from the links below or find my social links on the home page.
            <br>
            <br>
            Also check out my blog, I write about visual art.
            <br>
            <br>
          </span>
        </span>
        <span class="about__link__container">
          <nuxt-link class="about__link" to="/resume">Resume</nuxt-link>  <nuxt-link class="about__link" to="/resume">Blog</nuxt-link>  <nuxt-link class="about__link" to="/resume">Github</nuxt-link>
        </span>
      </div>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss">
.about {
  margin: 0 auto;
  z-index: 100;
  position: fixed;
  top:0;
  right: 0;
  bottom: 0;
  left: 0;
  background-color: #727372;
  // transition: opacity .4s linear .4s;

  &__content {
    width: 50%;
    max-width: 700px;
    text-align: center;
    position: absolute;
    color: #fff;
    top: 50%;
    left: 50%;
    transform: translate(-50%,-50%);
  }
}

// .about__content {
//   width: 50%;
//   max-width: 700px;
//   text-align: center;
//   position: absolute;
//   color: #fff;
//   top: 50%;
//   left: 50%;
//   transform: translate(-50%,-50%);
// }

.content {
  font-family: EB Garamond;
  font-size: 20px;
}

</style>