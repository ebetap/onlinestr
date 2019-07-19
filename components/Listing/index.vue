<template>
  <div class="card-listing">
    <img :src="url" alt="Product Image" />
    <p class="product-name">Radiant Tee</p>
    <p class="price">$27.06</p>
  </div>
</template>

<script>
const url = `https://demo.storefrontcloud.io/img/310/300/resize/w/s/ws12-blue_main.jpg`
export default {
  name: 'Cardlisting',
  data() {
    return {
      url: url
    }
  },
  props: {
    data: Object
  }
}
</script>

<style scoped></style>
