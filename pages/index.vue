<template>
  <div class="homepage">
    <Hero :imageUrl="heroUrl" />
    <section class="home-listing">
      <div class="container">
        <h2 class="text-center">Everything New</h2>
        <div class="wrapper-list">
          <Listing />
        </div>
      </div>
    </section>
  </div>
</template>

<script>
import Listing from '@@/components/Listing'
import Hero from './components/Hero'
const urlHero = `http://getwallpapers.com/wallpaper/full/8/e/a/926893-free-download-nike-air-max-wallpaper-1920x1080-for-xiaomi.jpg`
export default {
  name: 'Homepage',
  components: {
    Hero,
    Listing
  },
  data() {
    return {
      heroUrl: urlHero
    }
  }
}
</script>

<style>
.home-listing {
  padding: 20px 0;
}
.home-listing h2 {
  font-weight: bold;
}
.wrapper-list {
  display: flex;
}
</style>
