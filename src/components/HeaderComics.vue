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
.container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    background-color: white;
    height: 100px;
    font-weight: 600;

    img {
        width: 70px;
    }

    nav {
        flex: 0 1 60%;
        height: 100%;

        ul {
            display: flex;
            justify-content: space-between;
            height: 100%;

            li {
                display: inline-block;
                height: 100%;

                a {
                    display: inline-block;
                    text-decoration: none;
                    color: black;
                    text-transform: uppercase;
                    line-height: 100px;
                    vertical-align: middle;
                    color: #616161;
                }
            }
        }
    }
}
</style>