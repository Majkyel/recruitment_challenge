<template>
<div class="pageInformation">
  <div class="pageInformation__container container">
    <div class="pageInformation__content first__content">
      <p class="pageInformation__text">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam vitae lorem euismod, dapibus urna sit amet, viverra nunc. Fusce convallis felis quis porttitor auctor. Etiam enim massa, accumsan eu ipsum in, pellentesque egestas lorem. Nunc
        consectetur felis sit amet nibh dapibus, vitae molestie turpis lacinia. Nullam non bibendum nisi, tempus porttitor mi. Quisque nec eros vitae dui efficitur interdum. Ut pulvinar leo odio, nec pulvinar augue lacinia vel. Vivamus est erat,
        tristique quis arcu quis, molestie varius nulla. Mauris placerat pulvinar ex, in volutpat tortor semper ac. Pellentesque imperdiet felis a mattis mollis. Pellentesque ornare quis ante id auctor. Fusce sed sem luctus, hendrerit mauris a,
        fringilla urna. Etiam tristique, arcu ac feugiat dictum.
      </p>
    </div>
    <div class="pageInformation__content second__second">
      <p class="pageInformation__text">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam vitae lorem euismod, dapibus urna sit amet, viverra nunc. Fusce convallis felis quis porttitor auctor. Etiam enim massa, accumsan eu ipsum in, pellentesque egestas lorem. Nunc
        consectetur felis sit amet nibh dapibus, vitae molestie turpis lacinia. Nullam non bibendum nisi, tempus porttitor mi. Quisque nec eros vitae dui efficitur interdum. Ut pulvinar leo odio, nec pulvinar augue lacinia vel. Vivamus est erat,
        tristique quis arcu quis, molestie varius nulla. Mauris placerat pulvinar ex, in volutpat tortor semper ac. Pellentesque imperdiet felis a mattis mollis. Pellentesque ornare quis ante id auctor. Fusce sed sem luctus, hendrerit mauris a,
        fringilla urna. Etiam tristique, arcu ac feugiat dictum.
      </p>
    </div>
    <div class="pageInformation__content third__third">
      <p class="pageInformation__text">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam vitae lorem euismod, dapibus urna sit amet, viverra nunc. Fusce convallis felis quis porttitor auctor. Etiam enim massa, accumsan eu ipsum in, pellentesque egestas lorem. Nunc
        consectetur felis sit amet nibh dapibus, vitae molestie turpis lacinia. Nullam non bibendum nisi, tempus porttitor mi. Quisque nec eros vitae dui efficitur interdum. Ut pulvinar leo odio, nec pulvinar augue lacinia vel. Vivamus est erat,
        tristique quis arcu quis, molestie varius nulla. Mauris placerat pulvinar ex, in volutpat tortor semper ac. Pellentesque imperdiet felis a mattis mollis. Pellentesque ornare quis ante id auctor. Fusce sed sem luctus, hendrerit mauris a,
        fringilla urna. Etiam tristique, arcu ac feugiat dictum.
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
                text-indent: -12px;
                text-align: justify;
                word-break: break-word;
                margin: 10px;
                font-size: 19px;
                letter-spacing: 1px;
            }
        }
    }
}

@media screen and (max-width: 680px) {
    .pageInformation__container {
        display: block!important;
    }
}
</style>
