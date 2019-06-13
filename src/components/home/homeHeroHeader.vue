<template>
<div class="heroHeader">
  <div class="heroHeader__container container">
    <h1 class="heroHeader__title">power source</h1>
  </div>
</div>
</template>

<script>
export default {
  name: 'heroHeader',
};
</script>

<style lang="scss" scoped>
.heroHeader {
    background-image: url("../../../public/images/hero_header.jpeg");
    height: calc(100vh - 100px);
    background-size: cover;
    background-repeat: no-repeat;
    display: flex;
    .heroHeader__container {
        .heroHeader__title {
            text-transform: uppercase;
            font-size: calc(3vw + 3vh);
            text-shadow: 0 0 5px yellow;
            color: black;
            font-weight: 900;
            letter-spacing: 5px;
            opacity: 0.5;
            animation-name: titleAnimation;
            animation-duration: 4s;
        }
    }
}
@keyframes titleAnimation {
    from {
        opacity: 0;
    }
    to {
        opacity: 0.5;
    }
}
</style>
