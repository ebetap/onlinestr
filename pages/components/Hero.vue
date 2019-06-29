<template>
  <div class="hero-image" :style="{ background: imageUrl }">

  </div>
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
    subTitle: String,
  }
}
</script>

<style>

</style>
