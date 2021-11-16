<template>
  <div id="app">
    <Header></Header>
    <main>
      <SongsContainer></SongsContainer>
    </main>
  </div>
</template>

<script>
import SongsContainer from "./components/SongsContainer.vue";
import Header from "./components/Header.vue";
export default {
  components: {
    SongsContainer,
    Header,
  },
  name: "App",
};
</script>

<style lang="scss">
@import "@/styles/app";
@import "@/styles/variables.scss";
</style>
