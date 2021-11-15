<template>
  <div class="container my-5">
    <div class="row row-cols-1 row-cols-md-5 g-5">
      <div class="col" v-for="(song, i) in songsList" :key="i">
        <SongCard
          :image="song.poster"
          :title="song.title"
          :author="song.author"
          :year="song.year"
        ></SongCard>
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";
import SongCard from "./SongCard.vue";
export default {
  components: { SongCard },
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