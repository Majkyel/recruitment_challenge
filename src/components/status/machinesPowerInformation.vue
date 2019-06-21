<template>
<div class="machinesPower">
  <div class="machinesPower__container container">
    <h2 class="machinesPower__title">TOTAL POWER: {{totalPower}} kW</h2>
    <div class="machinesPower__content">
      <div class="machinesPower__content--consumption first-content" @click="powerMechanismMileniumFalcon">
        <div class="machinesPower__image" :class={isActive:mileniumIsActive}>
          <img class="image__first" src="../../../public/images/falcon.jpg" alt="Milenium Falcon">
        </div>
        <div class="machinesPower--consumption">{{mileniumFalconPower}} kW</div>
      </div>
      <div class="machinesPower__content--consumption second-content" @click="powerMechanismLightsaber">
        <div class="machinesPower__image" :class={isActive:lightsaberIsActive}>
          <img class="image__second" src="../../../public/images/lightsaber.png" alt="Lightsaber">
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
        margin: 20vh auto;
        .machinesPower__title {}
        .machinesPower__content {
            display: flex;
            justify-content: space-around;
            margin: 50px 0;
            .machinesPower__content--consumption {
                cursor: pointer;
                .machinesPower__image {
                    height: 300px;
                    width: 300px;
                    border: 2px solid gray;
                    box-shadow: 0 0 13px gray;
                    border-radius: 100%;
                    overflow: hidden;
                    filter: saturate(8%);
                    img {
                        display: block;

                        margin-left: auto;
                        margin-right: auto;
                        margin-top: 50%;
                        transform: translateY(-50%);
                    }
                    .image__first {
                        width: 90%;
                    }
                    .image__second {
                        width: 80%;
                    }
                }
                .machinesPower--consumption {
                    color: black;
                    font-size: 24px;
                    margin: 13px 0;
                }
                .isActive {
                    border: 2px solid green;
                    box-shadow: 0 0 13px green;
                    filter: saturate(100%);
                }
            }
            .first-content {}
            .second-content {}
        }
    }
}
@media screen and (max-width: 680px) {
    .machinesPower__content {
        display: block!important;
        .machinesPower__image {
            margin: auto!important;
        }
    }
}
@media screen and (max-width: 420px) {
    .machinesPower__container {
        margin: 14vh auto!important;
        .machinesPower__content {
            .machinesPower__content--consumption {
                margin-bottom: 35px!important;
                .machinesPower__image {
                    height: 220px!important;
                    width: 220px!important;
                }
            }
        }
    }
}
@media screen and (max-width: 360px) {
    .machinesPower__container {
        margin: 10vh auto!important;
        .machinesPower__content {
            .machinesPower__content--consumption {
                margin-bottom: 35px!important;
                .machinesPower__image {
                    height: 200px!important;
                    width: 200px!important;
                }
            }
        }
    }
}
</style>
