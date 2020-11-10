<template>
  <div class="about">
      <nav class="navbar">
        <nuxt-link to="/" class="navbar-link">Home</nuxt-link>
      </nav>
      <div class="about-content">
        <span class="content">
          <span>
            Hello. This website is made purely for fun and anything over here has no intentional resemblance to any individual or a particular event.
            <br>
            <br>
            I hope you, good fella', understand.
          </span>
        </span>
      </div>
  </div>
</template>

<script>
export default {

}
</script>

<style>
.about {
    margin: 0 auto;
  z-index: 100;
  position: fixed;
  top:0;
  right: 0;
  bottom: 0;
  left: 0;
  background-color: #727372;
}

.about-content {
  width: 50%;
  max-width: 700px;
  text-align: center;
  position: absolute;
  color: #fff;
  top: 50%;
  left: 50%;
  transform: translate(-50%,-50%);
}

.content {
  font-family: EB Garamond;
  font-size: 20px;
}

</style>