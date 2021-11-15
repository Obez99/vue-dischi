<template>
  <div class="card p-3 h-100">
    <img class="card-img-top" :src="image" />
    <div class="card-body text-center">
      <h5 class="card-title text-white text-uppercase">
        {{ title }}
      </h5>
      <p class="card-text text-secondary mb-0">
        {{ author }}
      </p>
      <p class="card-text text-secondary">
        {{ year }}
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: "SongCard",
  props: {
    image: String,
    title: String,
    author: String,
    year: String,
  },
};
</script>