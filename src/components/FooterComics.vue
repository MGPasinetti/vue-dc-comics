<template>
  <footer>
        <section class="dc-buy">
            <div class="container">
                <ul>
                    <li v-for="link in links" :key="link">
                        <a :href="link.href">
                            <img :src="link.src" :alt="link.text">
                            {{link.text}}
                        </a>
                    </li>
                </ul>
            </div>
        </section>

        <section class="nav-footer">
            <div class="container"></div>
        </section>

        <section class="socials">
            <div class="container"></div>
        </section>
  </footer>
</template>

<script>
export default {
    name: `FooterComics`,
    data () {
        return {
            links: [
                {
                    href: `#`,
                    src: require(`../assets/img/buy-comics-digital-comics.png`),
                    text: `digital comics`,
                },
                {
                    href: `#`,
                    src: require(`../assets/img/buy-comics-merchandise.png`),
                    text: `dc merchandise`,
                },
                {
                    href: `#`,
                    src: require(`../assets/img/buy-comics-subscriptions.png`),
                    text: `subscription`,
                },
                {
                    href: `#`,
                    src: require(`../assets/img/buy-comics-shop-locator.png`),
                    text: `comic shop locator`,
                },
                {
                    href: `#`,
                    src: require(`../assets/img/buy-dc-power-visa.svg`),
                    text: `dc power visa`,
                }
            ]
        }
    }, 
}
</script>

<style scoped lang="scss">
@import "../assets/styles/partials/variables.scss";


footer {
    .dc-buy {
        height: 150px;
        background-color: $blue_color;

        ul {
            height: 100%;
            display: flex;
            justify-content: space-around;
            color: white;

            li {
                display: inline-block;
                height: 100%;

                a {
                    text-decoration: none;
                    text-transform: uppercase;
                    color: white;
                    line-height: 150px;
                    vertical-align: middle;
                    display: flex;
                    align-items: center;

                    img {
                        height: 3.5rem;
                        margin-right: 1rem;
                    }
                }
            }
        }
    }
}
</style>