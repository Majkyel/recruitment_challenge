<template>
<div class="home">
  <Information />
</div>
</template>

<script>
import Information from '@/components/Information.vue';

export default {
  name: 'home',
  components: {
    Information,
  }
};
</script>

<style lang="scss" scoped>
.home {
    .home__title {
        font-size: 35px;
        margin: 15px;
    }
    .home__subtitle {
        font-size: 25px;
        margin: 15px;
    }
    .home__branches {
        margin-top: 30px;
    }
}
</style>
