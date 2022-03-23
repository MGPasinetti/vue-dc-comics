<template>
  <header>
      <div class="container">
        <img src="../assets/img/dc-logo.png" alt="">
        <nav>
            <ul>
                <li v-for="(link, index) in links" :key="index" @click="setActiveIndex(index)" :class="{active: index == activeIndex }">
                    <a :href="link.href">{{link.text.toUpperCase()}}</a>
                </li>
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
            activeIndex: 0,
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
    methods: {
        setActiveIndex (index) {
            this.activeIndex = index;
        },
    }
}
</script>

<style scoped lang="scss">
@import "../assets/styles/partials/variables.scss";

header {
    background-color: white;

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
                        line-height: 100px;
                        vertical-align: middle;
                        color: #616161;
                    }
                    &.active a {
                        color: $blue_color;
                    }
                    &.active {
                        border-bottom: 4px solid $blue_color;
                    }
                }
            }
        }
    }
}
</style>