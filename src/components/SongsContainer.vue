<template>
  <div class="container my-5">
    <div class="loading-screen" v-if="!isLoaded">
      <img src="../assets/logo.png" alt="" />
      <div class="loader">
        <div class="point point1"></div>
        <div class="point point2"></div>
        <div class="point point3"></div>
      </div>
    </div>
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
      isLoaded: false,
    };
  },
  mounted() {
    axios
      .get("https://flynn.boolean.careers/exercises/api/array/music")
      .then((response) => {
        this.songsList = response.data.response;

        //La schermata di caricamento viene visualizzata solo dopo che l'API viene caricato, ma ho impostato un timer di 2 secondi a scopo didattico
        setTimeout(() => {
          this.isLoaded = true;
        }, 2000);
      });
  },
};
</script>

<style lang="scss">
@import "@/styles/loading.scss";
</style>