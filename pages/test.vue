<template>
  <div class="container mainwindow">
      <div class="menu_wrapper">
        <div class="menubg"></div>
        <span class="line__top"></span>
        <span class="line__bottom"></span>
        <span class="line__left"></span>
        <span class="line__right"></span>
      </div>
  </div>
</template>

<script>
import * as THREE from "three";

export default {
  head: {
    title: "Kushal | Test",
  },

  mounted: function() {
  }
};
</script>

<style lang="scss">
.line{
  
  &__top{
    transform-origin: top left;
    top:0;
    left:0;
    width: 100%;
    height: 2px;
    background-color: var(--color-2);
    transition: transform 1.2s cubic-bezier(1,0,0,1) .8s,background-color .4s linear,-webkit-transform 1.2s cubic-bezier(1,0,0,1) .8s;
    display: block;
  position: absolute;
  z-index: 4;
  }
  &__bottom{
    width: 100%;
    height: 2px;
    background-color: var(--color-2);
    bottom: 0;
    right: 0;
    transform-origin: bottom right;
    transition: transform 1.2s cubic-bezier(1,0,0,1) .8s,background-color .4s linear,-webkit-transform 1.2s cubic-bezier(1,0,0,1) .8s;
    display: block;
  position: absolute;
  z-index: 4;
  }
  &__right{
    width: 2px;
    height: 100%;
    background-color: var(--color-2);
    top: 0;
    right: 0;
    transform-origin: top right;
    transition: transform 1.2s cubic-bezier(1,0,0,1) .8s,background-color .4s linear,-webkit-transform 1.2s cubic-bezier(1,0,0,1) .8s;
    display: block;
  position: absolute;
  z-index: 4;
  }
  &__left{
    width: 2px;
    height: 100%;
    transform-origin: bottom left;
    bottom: 0;
    left: 0;
    background-color: var(--color-2);
    transition: transform 1.2s cubic-bezier(1,0,0,1) .8s,background-color .4s linear,-webkit-transform 1.2s cubic-bezier(1,0,0,1) .8s;
    display: block;
  position: absolute;
  z-index: 4;
  }
}
.mainwindow{
  transition: opacity .4s linear .4s;
}

.menu_wrapper{
  top: 20px;
  bottom:auto;
  left: 20px;
  right: 20px;
  height: 104px;
  display: flex;
  flex-wrap: nowrap;
  flex-direction: row;
  overflow: hidden;
  z-index: 90;
  position: fixed;
}

</style>