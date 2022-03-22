<template>
  <header>
      <div class="container">
        <img src="../assets/img/dc-logo.png" alt="">
        <nav>
            <ul>
                <li v-for="(link, index) in links" :key="index"><a :href="link.href">{{link.text}}</a></li>
            </ul>
        </nav>
      </div>
  </header>
</template>

<script>
export default {
    name: `HeaderComics`,
    data () {
        return {
            links: [
                {
                    href: `#`,
                    text: `Characters`
                },
                {
                    href: `#`,
                    text: `Comics`
                },
                {
                    href: `#`,
                    text: `Movies`
                },
                {
                    href: `#`,
                    text: `Tv`
                },
                {
                    href: `#`,
                    text: `Games`
                },
                {
                    href: `#`,
                    text: `Collectibles`
                },
                {
                    href: `#`,
                    text: `Videos`
                },
                {
                    href: `#`,
                    text: `Fans`
                },
                {
                    href: `#`,
                    text: `News`
                },
                {
                    href: `#`,
                    text: `Shop`
                }
            ],
        }
    },
}
</script>

<style scoped lang="scss">
li {
    display: inline-block;
    a {
        display: inline-block;
        text-decoration: none;
        color: black;
    }
}
</style>