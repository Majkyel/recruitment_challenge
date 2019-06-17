<template>
<div class="home">
  <heroHeader />
  <pageInformation />
</div>
</template>

<script>
import heroHeader from '@/components/home/heroHeader.vue';
import pageInformation from '@/components/home/homePageInformation.vue';

export default {
  name: 'home',
  components: {
    heroHeader,
    pageInformation
  },
};
</script>

<style lang="scss" scoped>

</style>
