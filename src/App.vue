<template>
<div id="app" class="app">
  <Header />
  <transition name="fade" mode="out-in">
    <router-view />
  </transition>
  <div class="app__arrow--up" @click="clickGoUp(scrollTopSpeed)"></div>
  <Footer />
</div>
</template>

<script>
import Header from './views/Header.vue';
import Footer from './views/Footer.vue';

export default {
  data: function() {
    return {
      scrollTopSpeed: 800
    }
  },
  components: {
    Header,
    Footer
  },
  methods: {
    clickGoUp: function(scrollDuration) {
      let scrollStep = -window.scrollY / (scrollDuration / 15),
        scrollInterval = setInterval(function() {
          if (window.scrollY != 0) {
            window.scrollBy(0, scrollStep);
          } else clearInterval(scrollInterval);
        }, 15);
    }
  },
  created: function() {
    window.addEventListener("scroll", function(event) {
      let scroll = this.scrollY;
      let arrowUpButton = document.querySelector('.app__arrow--up');
      (scroll > 150) ? arrowUpButton.style.display = 'block': arrowUpButton.style.display = 'none';
    });
  }
}
</script>

<style lang="scss">
@import "./scss/_variables.scss";

.fade-enter-active,
.fade-leave-active {
    transition-duration: .3s;
    transition-property: opacity;
    transition-timing-function: ease;
}
.fade-enter,
.fade-leave-active {
    opacity: 0;
}
body {
    margin: 0;
}
.app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: $app-font-color;
    min-height: 100vh;
    overflow: hidden;
    .app__arrow--up {
        position: fixed;
        padding: 1vh 1.5vh;
        background: $app-arrow-up-background;
        color: $app-arrow-up-color;
        bottom: 70px;
        right: 40px;
        display: none;
        cursor: pointer;
        border-radius: 7px;
        border: 1.2px solid $app-arrow-up-border;
        box-shadow: 1px 1px 5px $app-arrow-up-box-shadow;
        &::after {
            content: '⇧';
            font-size: 1.6em;
            -webkit-text-fill-color: $app-arrow-up-fill;
        }
    }
}
.container {
    max-width: 1366px;
    margin: auto;
}
</style>
