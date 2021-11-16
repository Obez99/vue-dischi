<template>
  <div>
    <h2 class="mb-3 text-black">Filtra per genere</h2>
    <select
      v-model="choice"
      class="form-select mb-5"
      @change="$emit('genreChange', choice)"
    >
      <option selected value="">Tutti i generi</option>
      <option v-for="(genre, i) in genres" :key="i" :value="genre">
        {{ genre }}
      </option>
    </select>
  </div>
</template>

<script>
export default {
  name: "FilterSelect",
  props: { genres: Array },
  data() {
    return {
      choiche: "",
    };
  },
};
</script>

<style lang="scss">
@import "../styles/select.scss";
</style>