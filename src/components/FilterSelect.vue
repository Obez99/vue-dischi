<template>
  <select class="form-select mb-5">
    <option selected>Filtra per genere</option>
    <option v-for="(genre, i) in genres" :key="i">{{ genre }}</option>
  </select>
</template>

<script>
export default {
  name: "FilterSelect",
  props: { genres: Array },
};
</script>

<style lang="scss">
@import "../styles/select.scss";
</style>