<template>
<div class="header">
  <div class="navigation__container container">
    <div id="nav" class="navigation__content">
      <div class="navigation__logo">
        <a class="logo__link" href="/">
          <Logo width="150px" height="100px" />
        </a>
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
.header {
    height: 100px;
    .navigation__container {
        .navigation__content {
            padding: 0 30px;
            display: flex;
            justify-content: space-between;
            .link {
                font-weight: bold;
                color: #2c3e50;
                text-decoration: none;
                text-transform: uppercase;
                font-weight: bold;
                &.router-link-exact-active {
                    color: #42b983;
                }
            }
            .navigation__links {
                display: block;
                align-self: center;
                .navigation__link {
                    margin: 0 15px;
                    padding: 2px;
                    letter-spacing: 2px;
                    font-weight: 900;
                }
            }
            .hamburger__menu {
                display: none;
            }
        }
    }
}
</style>
