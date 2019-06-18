<template>
<div class="machinesPower">
  <div class="machinesPower__container container">
    <h2 class="machinesPower__title">TOTAL POWER: {{totalPower}} kW</h2>
    <div class="machinesPower__content">
      <div class="machinesPower__content--consumption first-content" @click="powerMechanismMileniumFalcon">
        <div class="machinesPower__image" :class={isActive:mileniumIsActive}>
          <img src="" alt="Milenium Falcon">
        </div>
        <div class="machinesPower--consumption">{{mileniumFalconPower}} kW</div>
      </div>
      <div class="machinesPower__content--consumption second-content" @click="powerMechanismLightsaber">
        <div class="machinesPower__image" :class={isActive:lightsaberIsActive}>
          <img src="" alt="Lightsaber">
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
  },
  methods: {
    powerMechanismMileniumFalcon: function() {
      this.mileniumIsActive = !this.mileniumIsActive;
      if (this.mileniumIsActive === true) {
        let random = Math.floor(Math.random() * 8) + 1;
        this.mileniumFalconPower = random;
        this.totalPowerMechanism();
      } else {
        this.mileniumFalconPower = 0;
        this.totalPowerMechanism();
      }
    },
    powerMechanismLightsaber: function() {
      this.lightsaberIsActive = !this.lightsaberIsActive;
      if (this.lightsaberIsActive === true) {
        let random = Math.floor(Math.random() * 8) + 1;
        this.lightsaberPower = random;
        this.totalPowerMechanism();
      } else {
        this.lightsaberPower = 0;
        this.totalPowerMechanism();
      }
    },
    totalPowerMechanism: function() {
      this.totalPower = this.mileniumFalconPower + this.lightsaberPower;
    }
  }
};
</script>

<style lang="scss" scoped>
.machinesPower {
    .machinesPower__container {
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
                    img {
                        display: block;
                    }
                }
                .isActive {
                    border: 2px solid green;
                }
            }
            .first-content {}
            .second-content {}
        }
    }
}
</style>
