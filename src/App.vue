<template>
  <div id="app">
    <!-- header  -->
    <siteHeader/>
    <!-- hero image  -->
    <heroImage/>
  </div>
</template>

<script>
// importazioni 
import siteHeader from './components/header.vue'
import heroImage from './components/heroImage.vue'
// font
import "@fontsource/montserrat"

export default {
  name: 'App',
  components: {
    siteHeader,
    heroImage
  }
}
</script>

<style lang="scss">
body { font-family: "Montserrat"; }
</style>
