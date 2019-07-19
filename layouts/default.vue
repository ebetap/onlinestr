<template>
  <div>
    <Navigation
      :menuOnClick="sideMenuHandler"
      :searchOnClick="searchHandler"
      :wishlistOnClick="wishlistHandler"
      :cartOnClick="cartHandler"
    />
    <Sidemenu :open="openSideMenu" :overlayOnClick="sideMenuHandler" />
    <Search :open="openSearch" :overlayOnClick="searchHandler" />
    <Wishlist :open="openWishlist" :overlayOnClick="wishlistHandler" />
    <Cart :open="openCart" :overlayOnClick="cartHandler" />
    <nuxt />
    <Footer />
  </div>
</template>
<script>
import Navigation from '@@/components/Navigation'
import Sidemenu from '@@/components/Sidemenu'
import Search from '@@/components/Search'
import Wishlist from '@@/components/Wishlist'
import Cart from '@@/components/Cart'
import Footer from '@@/components/Footer'
export default {
  components: {
    Navigation,
    Sidemenu,
    Search,
    Wishlist,
    Cart,
    Footer
  },
  data() {
    return {
      openSideMenu: false,
      openSearch: false,
      openWishlist: false,
      openCart: false
    }
  },
  methods: {
    sideMenuHandler() {
      this.openSideMenu = !this.openSideMenu
    },
    searchHandler() {
      this.openSearch = !this.openSearch
    },
    wishlistHandler() {
      this.openWishlist = !this.openWishlist
    },
    cartHandler() {
      this.openCart = !this.openCart
    }
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Playfair+Display:400,700|Roboto:400,700&display=swap&subset=greek');
html {
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}
body {
  font-family: 'Roboto', sans-serif;
}
h1,
h2,
h3,
h4,
h5 {
  font-family: 'Playfair Display', serif;
}
*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
}
.container {
  max-width: 80%;
  margin: auto;
}
.text-center {
  text-align: center;
}
</style>
