<template>
<div id="app" class="app">
  <Header />
  <transition  name="fade" mode="out-in">
      <router-view />
  </transition>
  <Footer />
</div>
</template>

<script>
import Header from './views/Header.vue';
import Footer from './views/Footer.vue';

export default {
  components: {
    Header,
    Footer
  }
}
</script>

<style lang="scss">
.fade-enter-active,
.fade-leave-active {
  transition-duration: 0.3s;
  transition-property: opacity;
  transition-timing-function: ease;
}

.fade-enter,
.fade-leave-active {
  opacity: 0
}

body {
    margin: 0;
}
.app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    min-height: 100vh;
    overflow: hidden;
}
.container {
    max-width: 1366px;
    margin: auto;
}
</style>
