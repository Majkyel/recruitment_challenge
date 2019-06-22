<template>
<div class="footer">
  <div class="footer__container container">
    <p class="footer__text">All rights... or not.</p>
  </div>
</div>
</template>

<script>

</script>

<style lang="scss" scoped>
@import "../scss/_variables.scss";

.footer {
    background-color: $footer-background-color;
    height: 40px;
    box-shadow: 0 -4px 7px $footer-box-shadow;
    .footer__container {
        padding: 10px;
        .footer__text {
            color: $footer-text-color;
            font-size: 14px;
            margin: 0;
        }
    }
}
</style>
