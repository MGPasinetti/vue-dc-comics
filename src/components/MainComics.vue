<template>
  <main>
      <div class="container">
          {{msg}}
      </div>
  </main>
</template>

<script>
export default {
    name: `MainComics`,
    data () {
        return {
            msg: `--> Content goes here <--`,
        }
    },
}
</script>

<style scoped lang="scss">
main {
    background-color: black;

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