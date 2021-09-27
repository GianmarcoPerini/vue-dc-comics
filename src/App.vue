<template>
  <div id="app">

    <Head />
    <Main />
    <Foot />

  </div>
</template>

<script>

import Head from './components/Head.vue'
import Main from './components/Main.vue'
import Foot from './components/Foot.vue'

export default {
  name: 'App',
  components: {
    Head,
    Main,
    Foot
  }
}
</script>


<style lang="scss">
@import './components/general.scss';



#app {
  font-family: $font;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  overflow-x: hidden;
}
</style>
