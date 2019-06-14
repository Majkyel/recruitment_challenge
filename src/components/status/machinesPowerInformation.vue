<template>
<div class="machinesPower">
  <div class="machinesPower__container container">
    <h2 class="machinesPower__title">TOTAL POWER: {{totalPower}} kW</h2>
    <div class="machinesPower__content">
      <div class="machinesPower__content--consumption first-content">
        <div class="machinesPower__image">
          <img src="" alt="">
        </div>
        <div class="machinesPower--consumption">{{mileniumFalconPower}} kW</div>
      </div>
      <div class="machinesPower__content--consumption second-content">
        <div class="machinesPower__image">
          <img src="" alt="">
        </div>
        <div class="machinesPower--consumption">{{lightsaberPower}} kW</div>
      </div>
    </div>
  </div>
</div>
</template>

<script>
export default {
  name: 'machinesPower',
  data: function() {
    return {
      totalPower: 0,
      mileniumFalconPower: 0,
      lightsaberPower: 0,
      mileniumIsActive: false,
      lightsaberIsActive: false
    }
  }
};
</script>

<style lang="scss" scoped>
.machinesPower {
    .machinesPower__container {
        padding: 100px 0;
        .machinesPower__title {}
        .machinesPower__content {
            display: flex;
            justify-content: space-around;
            margin: 50px 0;
            .machinesPower__content--consumption {
                .machinesPower__image {
                    height: 100px;
                    width: 100px;
                    border: 2px solid gray;
                    border-radius: 50px;

                }
            }
            .first-content {}
            .second-content {}
        }
    }
}
</style>
