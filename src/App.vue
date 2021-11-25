<template>
  <div id="app">
    <siteHeader/>
  </div>
</template>

<script>
import siteHeader from './components/header.vue'
import "@fontsource/montserrat"
export default {
  name: 'App',
  components: {
    siteHeader,
  }
}
</script>

<style lang="scss">
body { font-family: "Montserrat"; }
</style>
