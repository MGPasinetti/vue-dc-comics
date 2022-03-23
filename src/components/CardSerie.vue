<template>
  <div class="card-serie">
      <img :src="serieThumb" :alt="serieName">
      <h2>{{ serieName }}</h2>
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

<style>

</style>