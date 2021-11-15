<template>
  <div id="app">
    <header class="px-3 py-2">
      <img src="@/assets/logo.png" alt="logo" />
    </header>
    <main>
      <SongsContainer></SongsContainer>
    </main>
  </div>
</template>

<script>
import SongsContainer from "./components/SongsContainer.vue";
export default {
  components: { SongsContainer },
  name: "App",
};
</script>

<style lang="scss">
@import "@/styles/app";
@import "@/styles/header.scss";
@import "@/styles/variables.scss";
</style>
