<template>
<div class="pageInformation">
  <div class="pageInformation__container container">
    <div class="pageInformation__content first__content">
      <p class="pageInformation__text">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam vitae lorem euismod, dapibus urna sit amet, viverra nunc. Fusce convallis felis quis porttitor auctor. Etiam enim massa, accumsan eu ipsum in, pellentesque egestas lorem. Nuncconsectetur felis sit amet nibh dapibus, vitae molestie turpis lacinia. Nullam non bibendum nisi, tempus porttitor mi. Quisque nec eros vitae dui efficitur interdum. Ut pulvinar leo odio, nec pulvinar augue lacinia vel. Vivamus est erat,tristique quis arcu quis, molestie varius nulla. Mauris placerat pulvinar ex, in volutpat tortor semper ac. Pellentesque imperdiet felis a mattis mollis. Pellentesque ornare quis ante id auctor. Fusce sed sem luctus, hendrerit mauris a,fringilla urna. Etiam tristique, arcu ac feugiat dictum.
      </p>
    </div>
    <div class="pageInformation__content second__content">
      <p class="pageInformation__text">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam vitae lorem euismod, dapibus urna sit amet, viverra nunc. Fusce convallis felis quis porttitor auctor. Etiam enim massa, accumsan eu ipsum in, pellentesque egestas lorem. Nuncconsectetur felis sit amet nibh dapibus, vitae molestie turpis lacinia. Nullam non bibendum nisi, tempus porttitor mi. Quisque nec eros vitae dui efficitur interdum. Ut pulvinar leo odio, nec pulvinar augue lacinia vel. Vivamus est erat,tristique quis arcu quis, molestie varius nulla. Mauris placerat pulvinar ex, in volutpat tortor semper ac. Pellentesque imperdiet felis a mattis mollis. Pellentesque ornare quis ante id auctor. Fusce sed sem luctus, hendrerit mauris a,fringilla urna. Etiam tristique, arcu ac feugiat dictum.
      </p>
    </div>
    <div class="pageInformation__content third__content">
      <p class="pageInformation__text">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam vitae lorem euismod, dapibus urna sit amet, viverra nunc. Fusce convallis felis quis porttitor auctor. Etiam enim massa, accumsan eu ipsum in, pellentesque egestas lorem. Nuncconsectetur felis sit amet nibh dapibus, vitae molestie turpis lacinia. Nullam non bibendum nisi, tempus porttitor mi. Quisque nec eros vitae dui efficitur interdum. Ut pulvinar leo odio, nec pulvinar augue lacinia vel. Vivamus est erat,tristique quis arcu quis, molestie varius nulla. Mauris placerat pulvinar ex, in volutpat tortor semper ac. Pellentesque imperdiet felis a mattis mollis. Pellentesque ornare quis ante id auctor. Fusce sed sem luctus, hendrerit mauris a,fringilla urna. Etiam tristique, arcu ac feugiat dictum.
      </p>
    </div>
  </div>
</div>
</template>

<script>
export default {
  name: 'pageInformation',
};
</script>

<style lang="scss" scoped>
.pageInformation {
    border-top: 1px solid black;
    min-height: 60vh;
    display: flex;
    .pageInformation__container {
        display: flex;
        justify-content: space-between;
        padding: 10px;
        .pageInformation__content {
            padding: 10px;
            .pageInformation__text {
                text-align: justify;
                word-break: break-word;
                margin: 10px;
                font-size: 16px;
                letter-spacing: 1px;
                font-style: italic;
                text-shadow: 1px 1px 4px lightgray;
            }
        }
        .first__content,.second__content {
            border-right: 1px solid lightgray;
        }
        .third__content {
            border: none;
        }
    }
}
@media screen and (max-width: 680px) {
    .pageInformation__container {
        display: block!important;
        .first__content,.second__content {
            border: none!important;
        }
    }
}
</style>
