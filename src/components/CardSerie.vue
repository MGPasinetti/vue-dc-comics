<template>
  <div class="card-serie">
      <img :src="serieThumb" :alt="serieName">
      <h5>{{ serieName.toUpperCase() }}</h5>
  </div>
</template>

<script>
export default {
    name: `CardSerie`,
    props: {
        serieThumb: String,
        serieName: String,
    }
}
</script>

<style scoped lang="scss">
@import "../assets/styles/partials/mixins.scss";

    .card-serie {
        flex-basis: calc((100% / 6) - 6rem);
        margin-bottom: 3.5rem;

        img {
            @include img-layout(15rem, 15rem, cover, top);
        }

        h5 {
            margin-top: 1rem;
            font-size: 14px;
        }
    }
</style>