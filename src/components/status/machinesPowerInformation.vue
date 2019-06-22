<template>
<div class="machinesPower">
  <div class="machinesPower__container container">
    <h2 class="machinesPower__title">TOTAL POWER: {{totalPower}} kW</h2>
    <div class="machinesPower__content">
      <div class="machinesPower__content--consumption first-content">
        <div class="machinesPower__image">
          <img class="image__first" src="../../../public/images/falcon.jpg" alt="Milenium Falcon">
        </div>
        <div class="machinesPower--consumption">{{mileniumFalconPower}} kW</div>
      </div>
      <div class="machinesPower__content--consumption second-content">
        <div class="machinesPower__image">
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
      interval: null,
      totalPower: 0,
      mileniumFalconPower: 0,
      lightsaberPower: 0
    }
  },
  methods: {
    loadData: function() {
      fetch("https://challenge.codetain.com/api/v1/charging_status")
        .then(response => response.json())
        .then(data => {
          this.mileniumFalconPower = data.charging_status.falcon;
          this.lightsaberPower = data.charging_status.lightsaber;
          this.totalPowerMechanism();
        });
    },
    totalPowerMechanism: function() {
      this.totalPower = this.mileniumFalconPower + this.lightsaberPower;
    }
  },
  created: function() {
    this.loadData();
    this.interval = setInterval(
      function() {
        this.loadData();
      }.bind(this),
      10000
    );
  },
  beforeDestroy: function() {
    clearInterval(this.interval);
  }
};
</script>

<style lang="scss" scoped>
@import "../../scss/_variables.scss";

.machinesPower {
    .machinesPower__container {
        margin: 20vh auto;
        .machinesPower__title {
            text-shadow: 0px 0px 29px $machines-power-title-power-text-shadow;
        }
        .titlePowerActive {
            text-shadow: 0 0 17px $machines-power-title-active-power-text-shadow;
        }
        .machinesPower__content {
            display: flex;
            justify-content: space-around;
            margin: 50px 0;
            .machinesPower__content--consumption {
                cursor: pointer;
                .machinesPower__image {
                    height: 300px;
                    width: 300px;
                    border: 2px solid $machines-power-image-border;
                    box-shadow: 0 0 13px $machines-power-image-box-shadow;
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
                    margin: 18px 15px;
                    border: 2px solid $machines-power-consumption-border;
                    border-radius: 20px;
                }
                .isActive {
                    border: 2px solid $machines-power-image-isActive-border;
                    box-shadow: 0 0 13px $machines-power-image-isActive-box-shadow;
                    filter: saturate(100%);
                }
            }
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
