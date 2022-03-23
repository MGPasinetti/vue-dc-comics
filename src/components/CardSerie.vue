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
    .card-serie {
        flex-basis: calc((100% - 5rem) / 6);
    }
</style>