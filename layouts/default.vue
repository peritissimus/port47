<template>
  <div>
    <Nuxt />
  </div>
</template>



<style>

html {
  font-family: Montserrat;
}

body{
  overflow: hidden;
}

nuxt-link {
  padding: 20px;
}


a, div, canvas {
  margin: 0;
  padding: 0;
}


.navbar {
  width: 80%;
  position: fixed;
  top: 50px;
  left: 50%;
  color: #f2f2f2;
  transform: translateX(-50%);
  text-align: right;
  z-index: 10;
}

.navbar-link {
  font-size: 14px;
  padding: 30px 0;
  color: inherit;
  text-decoration: none;
  text-transform: uppercase;
  letter-spacing: 2.002px;
}

.container {
    position: absolute;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    display: -ms-flexbox;
    display: flex;
    -ms-flex-direction: column;
    flex-direction: column;
    -ms-flex-pack: center;
    justify-content: center;
  
}


.container {
  z-index: 1;
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}


</style>
