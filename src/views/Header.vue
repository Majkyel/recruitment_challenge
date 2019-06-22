<template>
<div class="header">
  <div class="navigation__container container">
    <div id="nav" class="navigation__content">
      <div class="navigation__logo">
        <a class="logo__link" href="/">
          <Logo width="150px" height="100px" />
        </a>
      </div>
      <div class="navigation__links" v-bind:class="{hamburger__navigation:hamburgerIsActive}">
        <div class="navigation__container-links" v-bind:class="{hamburger__links:hamburgerIsActive}">
          <router-link class="navigation__link link" to="/" @click.native="deactiveHamburgerMenu">Home</router-link>
          <router-link class="navigation__link link" to="/status" @click.native="deactiveHamburgerMenu">Status</router-link>
        </div>
      </div>
      <div class="hamburger__menu" v-bind:class="{hamburger__animation:hamburgerIsActive}" @click="activeHamburgerMenu">
        <div class="hamburger__container">
          <div class="hamburger__bar1"></div>
          <div class="hamburger__bar2"></div>
          <div class="hamburger__bar3"></div>
        </div>
      </div>
    </div>
  </div>
</div>
</template>

<script>
import Logo from './Logo/Logo.vue';

export default {
  data: function() {
    return {
      hamburgerIsActive: false
    }
  },
  components: {
    Logo,
  },
  methods: {
    activeHamburgerMenu: function() {
      this.hamburgerIsActive = !this.hamburgerIsActive;
      let body = document.querySelector('body');
      if (this.hamburgerIsActive) {
        body.style.overflow = "hidden";
      } else {
        body.style.overflow = "auto";
      }
    },
    deactiveHamburgerMenu: function() {
      let body = document.querySelector('body');
      if (this.hamburgerIsActive) {
        this.hamburgerIsActive = false;
        body.style.overflow = "auto";
      }
    }
  }
}
</script>

<style lang="scss" scoped>
.header {
    height: 100px;
    border-bottom: 1px solid black;
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
                border-bottom: 1.5px solid white;
                transition: border-bottom 1s;
                &:hover {
                    border-bottom: 1.5px solid black;
                }
                &.router-link-exact-active {
                    border-bottom: 1.5px solid black;
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
            .hamburger__navigation {
                display: block!important;
                position: absolute;
                left: 0;
                right: 0;
                bottom: 0;
                height: calc(100vh - 101px);
                background-color: white;
                z-index: 2;
                .hamburger__links {
                    position: relative;
                    top: 20%;
                    transform: translateY(-50%);
                    .navigation__link {
                        display: block;
                        font-size: calc(2vh + 2vw);
                        margin: 10px 25px;
                        border: 2px solid black;
                        transition: none;
                    }
                }
            }
            .hamburger__menu {
                display: none;
                align-self: center;
                cursor: pointer;
                .hamburger__container {
                    .hamburger__bar1,
                    .hamburger__bar2,
                    .hamburger__bar3 {
                        width: 30px;
                        height: 3px;
                        background-color: #000;
                        margin: 6px 0;
                        transition: 0.4s;
                    }
                }
            }
            .hamburger__animation .hamburger__bar1 {
                -webkit-transform: rotate(-45deg) translate(-5px, 6px);
                transform: rotate(-45deg) translate(-5px, 6px);
            }
            .hamburger__animation .hamburger__bar2 {
                opacity: 0;
            }
            .hamburger__animation .hamburger__bar3 {
                -webkit-transform: rotate(45deg) translate(-7px, -8px);
                transform: rotate(45deg) translate(-7px, -8px);
            }
        }
    }
}
@media screen and (max-width: 420px) {
    .navigation__links {
        display: none!important;
    }
    .hamburger__menu {
        display: flex!important;
    }
}
</style>
