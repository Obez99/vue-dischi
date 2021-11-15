<template>
  <div class="loading-screen">
    <img src="../assets/logo.png" alt="" />
    <div class="loader">
      <div class="point point1"></div>
      <div class="point point2"></div>
      <div class="point point3"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: "LoadingScreen",
};
</script>

<style lang="scss">
@import "../styles/loading.scss";
</style>