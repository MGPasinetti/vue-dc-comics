<template>
  <footer>
        <section class="dc-buy">
            <div class="container">
                <ul>
                    <li v-for="link in links" :key="link">
                        <a :href="link.href">
                            <img :src="link.imgHref" :alt="link.text">
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
                    imgHref: `../assets/img/buy-comics-digital-comics.png`,
                    text: `digital comics`,
                },
                {
                    href: `#`,
                    imgHref: `../assets/img/buy-comics-merchandise.png`,
                    text: `dc merchandise`,
                },
                {
                    href: `#`,
                    imgHref: `../assets/img/buy-comics-subscriptions.png`,
                    text: `subscription`,
                },
                {
                    href: `#`,
                    imgHref: `../assets/img/buy-comics-shop-locator.png`,
                    text: `comic shop locator`,
                },
                {
                    href: `#`,
                    imgHref: `../assets/img/buy-dc-power-visa.svg`,
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
    }
}
</style>