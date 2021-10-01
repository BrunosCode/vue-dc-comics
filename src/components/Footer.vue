<template>
<footer class="c-footerTop">
    <div class="l-container l-row l-row--spacebetween">

        <nav class="c-footerTop__nav l-col l-wrap">
            <ul v-for="(list, i) in nav" :key="i" 
            class="c-footerTop__list h-listReset">
                <li>
                    <h3 class="c-footerTop__subtitle">{{list.title}}</h3>
                </li>
                <li v-for="(link, i) in list.links" :key="i">
                    <a :href="link.url"
                    class="c-footerTop__link c-link l-row">{{link.text}}</a>
                </li>
            </ul>
        </nav>
        <img class="c-footerTop__img" src="../assets/images/dc-logo-bg.png" alt="">
    </div>
    <CtaBanner/>
</footer>
</template>

<script>
import CtaBanner from './CtaBanner.vue';

export default {
    name: "Footer",
    components: {
        CtaBanner
    },
    data: function() {
        return {
            nav: {
                comicsLinks: {
                    title: "DC Comics",
                    links: [
                        {
                            text: "Characters",
                            url: "#",
                        },
                        {
                            text: "Comics",
                            url: "#",
                        },
                        {
                            text: "Movies",
                            url: "#",
                        },
                        {
                            text: "Tv",
                            url: "#",
                        },
                        {
                            text: "Games",
                            url: "#",
                        },
                        {
                            text: "Videos",
                            url: "#",
                        },
                        {
                            text: "News",
                            url: "#",
                        },
                    ],
                },
                shopLinks: {
                    title: "Shop",
                    links: [
                        {
                            text: "Shop DC",
                            url: "#",
                        },
                        {
                            text: "Shop DC Collectibles",
                            url: "#",
                        },
                    ],
                },
                dcLinks: {
                    title: "DC",
                    links: [
                        {
                            text: "Terms Of Use",
                            url: "#",
                        },
                        {
                            text: "Privacy policy (New)",
                            url: "#",
                        },
                        {
                            text: "Ad Choices",
                            url: "#",
                        },
                        {
                            text: "Advertising",
                            url: "#",
                        },
                        {
                            text: "Jobs",
                            url: "#",
                        },
                        {
                            text: "Subscription",
                            url: "#",
                        },
                        {
                            text: "Talent Workshops",
                            url: "#",
                        },
                        {
                            text: "CPSC Certificates",
                            url: "#",
                        },
                        {
                            text: "Ratings",
                            url: "#",
                        },
                        {
                            text: "Shop Help",
                            url: "#",
                        },
                        {
                            text: "Contact Us",
                            url: "#",
                        },
                    ],
                },
                sitesLinks: {
                    title: "Sites",
                    links: [
                        {
                            text: "DC",
                            url: "#",
                        },
                        {
                            text: "MAD Magazine",
                            url: "#",
                        },
                        {
                            text: "DC Kids",
                            url: "#",
                        },
                        {
                            text: "DC Universe",
                            url: "#",
                        },
                        {
                            text: "Power Visa",
                            url: "#",
                        },
                    ],
                }
            }
        }
    }
}
</script>

<style scoped lang="scss">
@import "../assets/style/variables.scss";

.c-footerTop {
    background-image: url("../assets/images/footer-bg.jpg");
    background-position: center;
    background-size: cover;

    &__nav {
        max-height: 400px;
        padding: 2rem 0;
    }

    &__list {
        margin-right: 2rem;
        margin-bottom: .75rem;
    }

    &__subtitle {
        text-transform: uppercase;
        font-size: 1.25rem;
        font-weight: 700;
        color: white;
        margin-bottom: .75rem;
    }

    &__link {
        color: $gray-300;
        margin-bottom: .25rem;

        &:hover {
            color: white;
        }
    }

    &__img {
        height: 400px;
        width: 50%;
        object-fit: cover;
    }

}
</style>