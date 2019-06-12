<template>
<div class="navigation__container">
  <div id="nav" class="navigation__content">
    <div class="navigation__logo">
        <Logo width="100px" height="100px"/>
    </div>
    <div class="navigation__links">
        <router-link class="navigation__link link" to="/">Home</router-link>
        <router-link class="navigation__link link" to="/status">Status</router-link>
    </div>
    <div class="hamburger__menu">
      <router-link class="hamburger__link link" to="/">Home</router-link>
      <router-link class="hamburger__link link" to="/status">Status</router-link>
    </div>
  </div>
</div>
</template>

<script>
import Logo from './Logo/Logo.vue';

export default {
  components: {
      Logo,
  }
}
</script>

<style lang="scss" scoped>
.navigation__container {
    .navigation__content {
        padding: 30px;
        .link {
            font-weight: bold;
            color: #2c3e50;
            &.router-link-exact-active {
                color: #42b983;
            }
        }
        .navigation__links {
            display: block;
        }
        .hamburger__menu {
            display: none;
        }
    }
}
</style>
