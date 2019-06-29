<template>
  <div id="header">
    <div class="navigation container">
      <div class="item menu-btn">
        <a-icon type="appstore" @click="menuOnClick()" />
      </div>
      <div class="item logo">
        <img src="~~/assets/logo.svg" />
      </div>
      <div class="item menu-right">
        <div class="item">
          <a-icon type="search" />
        </div>
        <div class="item">
          <a-icon type="heart" />
        </div>
        <div class="item">
          <a-icon type="shopping-cart" />
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
  props: {
    menuOnClick: Function
  }
}
</script>

<style scoped>
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
</style>
