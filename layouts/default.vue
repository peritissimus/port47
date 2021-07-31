<template>
  <div>
    <div class="cursor">
      <div class="cursor__frame"></div>
      <div class="cursor__icon"></div>
    </div>
    <Nuxt />
  </div>
</template>

<script>

export default {
  mounted: function() {

    const cursor = document.querySelector('.cursor__frame');
    const cursorf = document.querySelector('.cursor__icon')
    document.addEventListener('mousemove', e => {
      cursor.setAttribute("style", "top: "+(e.pageY-33)+"px; left: "+(e.pageX-33)+"px");
      cursorf.setAttribute("style", "top: "+(e.pageY-14)+"px; left: "+(e.pageX-14)+"px");
    })


  }
}
</script>



<style lang="scss">

:root {
  --color-1: #f2f2f2;
  --color-2: #a6a6a6;
  --color-3: #595959;
  --color-4: #262626;
  --color-5: #0d0d0d;
}

html {
  font-family: Montserrat;
  background-color: var(--color-5);
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

.text {
  color: var(--color-1);  
}
.navbar {
  width: 80%;
  position: fixed;
  top: 50px;
  left: 50%;
  color: var(--color-1);
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

.cursor {

  position: fixed;
  pointer-events: none;
  z-index:100;



  &__frame{
    z-index: 100;
    width: 50px;
    height: 50px;
    border: 2px solid var(--color-1);
    border-radius: 50%;
    position: absolute;
    transition-duration: 250ms;
    transition-timing-function: ease-out;

  }

  &__icon {
    z-index:100;
    width: 12px;
    height:12px;
    border-radius: 50%;
    background-color: var(--color-1);
    transition-duration: 100ms;
    transition-timing-function: ease-out;
    position: absolute;

  }
}

.is_hovered{
  border: 2px solid var(--color-2);
  // background-color: var(--color-2);
  transform: scale(1.5);

}

.is_hidden{
  display: none;
}

.link_hover{
  transform: scale(1.25);

  &__icon{
    background-color: none;
    border:1px;
    display: none;
  }
}


.cursor__click{
  background-color: var(--color-5);
  mix-blend-mode: difference;
}

</style>
