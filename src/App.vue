<template>
  <div id="app">
    <header class="px-3 py-2">
      <img src="@/assets/logo.png" alt="logo" />
    </header>
    <main>
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
    </main>
  </div>
</template>

<script>
export default {
  name: "App",
};
</script>

<style lang="scss">
@import "@/styles/app";
@import "@/styles/header.scss";
@import "@/styles/variables.scss";
</style>
