<template>
  <div id="app">
    <!-- header  -->
    <siteHeader
    :navBar="navBar"
    />
    <!-- hero image  -->
    <heroImage/>
    <!-- MAIN  -->
    <siteMain />
  </div>
</template>

<script>
// importazioni 
import siteHeader from './components/header.vue'
import heroImage from './components/heroImage.vue'
import siteMain from './components/main.vue'
// font
import "@fontsource/montserrat"

export default {
  name: 'App',
  components: {
    siteHeader,
    heroImage,
    siteMain
  },
data() {
  return{
    navBar: [
      {
        name:'home',
        dd1: 'link1',
        dd2: 'link2',
        dd3:'link3'
      },
      {
        name:'pages',
        dd1: 'link1',
        dd2: 'link 2',
        dd3:'link 3'
      },
      {
        name:'courses',
        dd1: 'link1',
        dd2: 'link 2',
        dd3:'link 3'
      },
      {
        name:'features',
        dd1: 'link1',
        dd2: 'link 2',
        dd3:'link 3'
      },
      {
        name:'blog',
        dd1: 'link1',
        dd2: 'link 2',
        dd3:'link 3'
      },
      {
        name:'shop',
        dd1: 'link1',
        dd2: 'link 2',
        dd3:'link 3'
      }
    ]
  }
}
}
</script>

<style lang="scss">
body { font-family: "Montserrat"; }
</style>
