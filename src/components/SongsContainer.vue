<template>
  <div class="container my-5">
    <div class="row row-cols-1 row-cols-md-5 g-5">
      <div class="col">
        <div class="card p-3">
          <img class="card-img-top" />
          <div class="card-body">
            <h5 class="card-title text-white">Test</h5>
            <p class="card-text text-secondary">
              Lorem ipsum, dolor sit amet consectetur adipisicing elit. Aut
              velit nihil voluptas mollitia quas accusamus possimus eius
              numquam! Officiis impedit adipisci aspernatur alias! Ipsum,
              quaerat nesciunt dolore a similique veritatis?
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