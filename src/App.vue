<template>
  <div id="app">
    <Header/>
    <Main/>
    <Banner/>
    <FooterTop/>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Main from './components/Main.vue'
import Banner from './components/Banner.vue'
import FooterTop from './components/FooterTop.vue'

export default {
  name: 'App',
  components: {
    Header,
    Main,
    Banner,
    FooterTop
  }
}
</script>

<style lang="scss">
@import "./assets/style/variables.scss";
@import "./assets/style/common.scss";

#app {
  font-family: 'PT Sans Narrow', sans-serif;
}
</style>
