<template>
  <select class="form-select mb-5" @change="$emit('change')">
    <option selected>Filtra per genere</option>
    <option v-for="(genre, i) in genres" :key="i" :value="genre">
      {{ genre }}
    </option>
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