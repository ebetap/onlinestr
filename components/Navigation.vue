<template>
  <div id="header" :class="{ fixed: navFixed }">
    <div class="navigation container">
      <div class="item menu-btn">
        <a-icon type="appstore" @click="menuOnClick()" />
      </div>
      <div class="item logo">
        <nuxt-link to="/">
          <img src="~~/assets/logo.svg" />
        </nuxt-link>
      </div>
      <div class="item menu-right">
        <div class="item">
          <a-icon type="search" @click="searchOnClick()" />
        </div>
        <div class="item">
          <a-icon type="heart" @click="wishlistOnClick()" />
        </div>
        <div class="item">
          <a-icon type="shopping-cart" @click="cartOnClick()" />
        </div>
        <div class="item">
          <a-icon type="user" />
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'Navigation',
  data() {
    return {
      navFixed: false
    }
  },
  props: {
    menuOnClick: Function,
    searchOnClick: Function,
    wishlistOnClick: Function,
    cartOnClick: Function
  },
  mounted() {
    if (window) window.addEventListener('scroll', this.scrollHandler)
  },
  destroyed() {
    window.removeEventListener('scroll', this.scrollHandler)
  },
  methods: {
    scrollHandler(event) {
      if (window.pageYOffset > 50) {
        this.navFixed = true
      } else {
        this.navFixed = false
      }
    }
  }
}
</script>

<style scoped>
#header {
  transition: all ease 0.4s;
}
.container {
  max-width: 80%;
  margin: auto;
}
.navigation {
  display: flex;
  justify-content: space-between;
  padding: 10px 0;
}
.navigation .logo img {
  max-width: 40px;
  display: block;
  margin: auto;
}
.navigation .menu-btn {
  align-self: center;
  cursor: pointer;
}
.navigation .menu-btn .anticon {
  font-size: 22px;
}
.navigation .menu-right {
  display: flex;
  align-items: center;
  justify-content: flex-end;
}
.navigation .menu-right .item {
  font-size: 22px;
  margin-left: 15px;
  cursor: pointer;
}
.navigation > .item {
  max-width: 33.33%;
  flex: 0 0 33.33%;
}
.fixed {
  position: fixed;
  width: 100%;
  background: #fff;
}
</style>
