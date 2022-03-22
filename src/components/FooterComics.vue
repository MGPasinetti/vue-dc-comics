<template>
  <footer>
        <section class="dc-buy">
            <div class="container">
                <ul>
                    <li v-for="link in dcBuyLinks" :key="link">
                        <a :href="link.href">
                            <img :src="link.src" :alt="link.text">
                            {{link.text}}
                        </a>
                    </li>
                </ul>
            </div>
        </section>

        <section class="nav-footer">
            <div class="container">
                <ul v-for="navLink in navLinks" :key="navLink">
                    <li>
                        <h3>{{navLink.title}}</h3>
                    </li>
                    <li v-for="ulLink in navLinks.ulLinks" :key="ulLink">
                        <a :href="ulLink.href">{{ulLink.text}}</a>
                    </li>
                </ul>
            </div>
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
            dcBuyLinks: [
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
            ],
            navLinks: [
                {
                    title: `DC COMICS`,
                    ulLinks: [
                        {
                            href: `#`,
                            text: `Characters`,
                        },
                        {
                            href: `#`,
                            text: `Comics`,
                        },
                        {
                            href: `#`,
                            text: `Movies`,
                        },
                        {
                            href: `#`,
                            text: `TV`,
                        },
                        {
                            href: `#`,
                            text: `Games`,
                        },
                        {
                            href: `#`,
                            text: `Videos`,
                        },
                        {
                            href: `#`,
                            text: `News`,
                        },
                    ]
                    
                },
                {
                    title: `SHOP`,
                    ulLinks: [
                        {
                            href: `#`,
                            text: `Shop DC`,
                        },
                        {
                            href: `#`,
                            text: `Shop DC Collectibles`,
                        }
                    ]
                    
                },
                {
                    title: `DC`,
                    ulLinks: [
                        {
                            href: `#`,
                            text: `Terms Of Use`,
                        },
                        {
                            href: `#`,
                            text: `Privecy policy (New)`,
                        },
                        {
                            href: `#`,
                            text: `Ad Choices`,
                        },
                        {
                            href: `#`,
                            text: `Advertising`,
                        },
                        {
                            href: `#`,
                            text: `Jobs`,
                        },
                        {
                            href: `#`,
                            text: `Subscriptions`,
                        },
                        {
                            href: `#`,
                            text: `Talent Workshops`,
                        },
                        {
                            href: `#`,
                            text: `CPSC Certificates`,
                        },
                        {
                            href: `#`,
                            text: `Ratings`,
                        },
                        {
                            href: `#`,
                            text: `Shop Help`,
                        },
                        {
                            href: `#`,
                            text: `Contact Us`,
                        }
                    ]
                    
                },
                {
                    title: `SITES`,
                    ulLinks: [
                        {
                            href: `#`,
                            text: `DC`,
                        },
                        {
                            href: `#`,
                            text: `MAD Magazine`,
                        },
                        {
                            href: `#`,
                            text: `DC Kids`,
                        },
                        {
                            href: `#`,
                            text: `DC Universe`,
                        },
                        {
                            href: `#`,
                            text: `DC Power Visa`,
                        },
                    ]
                    
                }
            ],
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

    .nav-footer {
        height: 400px;
        background-image: url(../assets/img/footer-bg.jpg);
    }
}
</style>