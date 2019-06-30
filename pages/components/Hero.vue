<template>
  <div class="hero-image" :style="{ background: `url(${imageUrl})` }"></div>
</template>

<script>
export default {
  name: 'Hero',
  props: {
    imageUrl: {
      type: String,
      required: true
    },
    title: String,
    subTitle: String
  }
}
</script>

<style>
.hero-image {
  height: 640px;
  background-size: cover !important;
}
</style>
