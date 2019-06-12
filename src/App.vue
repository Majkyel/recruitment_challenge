<template>
<div id="app" class="app">
  <Header />
  <router-view />
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
body {
    margin: 0;
}
.app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
}
.container {
    max-width: 1366px;
    margin: auto;
}
</style>
