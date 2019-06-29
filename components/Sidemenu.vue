<template>
  <div class="container-side-menu">
    <div class="side-menu" :class="{ open: open }">
      sidemenu
    </div>
    <div
      class="overlay"
      :class="{ 'open-o': open }"
      @click="overlayOnClick"
    ></div>
  </div>
</template>

<script>
export default {
  name: 'Sidemenu',
  props: {
    open: Boolean,
    overlayOnClick: Function
  }
}
</script>

<style scoped>
.side-menu {
  position: fixed;
  width: 0px;
  height: 100vh;
  background: #ffffff;
  top: 0;
  transition: width 0.2s;
  overflow: hidden;
  z-index: 2;
}
.overlay {
  top: 0;
  position: fixed;
  left: 0;
  bottom: 0;
  right: 0;
  background: #000;
  opacity: 0.4;
  display: none;
  transition: display 0.2s;
}
.open {
  width: 350px;
}
.open-o {
  display: block;
}
</style>
