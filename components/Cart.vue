<template>
  <div class="container-search">
    <div class="cart-popup" :class="{ open: open }">
      Cart
    </div>
    <div
      class="overlay-c"
      :class="{ 'open-o': open }"
      @click="overlayOnClick"
    ></div>
  </div>
</template>

<script>
export default {
  name: 'Wishlist',
  props: {
    open: Boolean,
    overlayOnClick: Function
  }
}
</script>

<style scoped>
.cart-popup {
  position: fixed;
  width: 0px;
  height: 100vh;
  background: #ffffff;
  top: 0;
  right: 0;
  transition: width 0.2s;
  overflow: hidden;
  z-index: 2;
}
.overlay-c {
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
  width: 60vw;
}
.open-o {
  display: block;
}
</style>
