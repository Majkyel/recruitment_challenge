<template>
<div class="home">
  <h1 class="home__title">RECRUITMENT CHALLENGE</h1>
  <h2 class="home__subtitle">CHECK THIS OUT!</h2>
  <h3 class="home__branches">BRANCHES:</h3>
  <p class="home__branch"><b>1. step_one_branch</b> >> there is step one task.</p>
  <p class="home__branch"><b>2. step_two_branch</b> >> there is step two task.</p>
</div>
</template>

<script>
export default {
  name: 'home',
};
</script>

<style lang="scss" scoped>
.home {
    .home__title {
        font-size: 35px;
        margin: 15px;
    }
    .home__subtitle {
        font-size: 25px;
        margin: 15px;
    }
    .home__branches {
        margin-top: 30px;
    }
}
</style>
