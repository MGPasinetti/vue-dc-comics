<template>
  <main>
      <img src="../assets/img/jumbotron.jpg" alt="">
      <div class="container">
      </div>
  </main>
</template>

<script>
export default {
    name: `MainComics`,
    data () {
        return {
        }
    },
}
</script>

<style scoped lang="scss">
main {
    background-color: black;

    img {
        width: 100%;
        height: 430px;
        object-fit: cover;
        object-position: top;
    }

    .container {
        height: 120px;
        color: white;
        display: flex;
        align-items: center;
        font-size: 25px;
        font-weight: 600;
    }
}
</style>