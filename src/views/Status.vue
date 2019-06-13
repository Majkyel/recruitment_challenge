<template>
<div class="status">
  <heroHeader />
  <machinesPower />
</div>
</template>

<script>
import heroHeader from '@/components/heroHeader.vue';
import machinesPower from '@/components/status/machinesPowerInformation.vue';

export default {
  components: {
    heroHeader,
    machinesPower
  }
}
</script>

<style lang="scss" scoped>

</style>
