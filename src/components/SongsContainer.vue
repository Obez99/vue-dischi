<template>
  <div class="container my-5">
    <div class="row row-cols-1 row-cols-md-5 g-5">
      <div class="col" v-for="(song, i) in songsList" :key="i">
        <div class="card p-3 h-100">
          <img class="card-img-top" :src="song.poster" />
          <div class="card-body text-center">
            <h5 class="card-title text-white text-uppercase">
              {{ song.title }}
            </h5>
            <p class="card-text text-secondary mb-0">
              {{ song.author }}
            </p>
            <p class="card-text text-secondary">
              {{ song.year }}
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";
export default {
  name: "SongsContainer",
  data() {
    return {
      songsList: [],
    };
  },
  mounted() {
    axios
      .get("https://flynn.boolean.careers/exercises/api/array/music")
      .then((response) => {
        this.songsList = response.data.response;
      });
  },
};
</script>