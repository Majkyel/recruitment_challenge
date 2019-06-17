<template>
<div class="status">
  <machinesPower />
</div>
</template>

<script>
import machinesPower from '@/components/status/machinesPowerInformation.vue';

export default {
  components: {
    machinesPower
  }
}
</script>

<style lang="scss" scoped>
.status {
  min-height: calc(100vh - 140px);
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>
