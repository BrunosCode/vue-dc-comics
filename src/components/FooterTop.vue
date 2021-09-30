<template>
<div :style="{backgroundImage: `url(${require('@/assets/images/footer-bg.jpg')})` }"
class="c-footerTop">
    <div class="l-container l-row l-row--spacebetween">

        <nav class="c-footerTop__nav l-col l-wrap">
            <ul v-for="(list, i) in nav" :key="i" 
            class="c-footerTop__list h-listReset">
                <li>
                    <h3 class="c-footerTop__subtitle">{{list.titole}}</h3>
                </li>
                <li v-for="(link, i) in list.links" :key="i">
                    <a :href="link.url"
                    class="c-footerTop__link c-link l-row">{{link.text}}</a>
                </li>
            </ul>
        </nav>
        <img class="c-footerTop__img" src="@/assets/images/dc-logo-bg.png" alt="">
    </div>
</div>
</template>

<script>
export default {
    name: "FooterTop",
    data: function() {
        return {
            nav: {
                comicsLinks: {
                    titole: "DC Comics",
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
                    titole: "Shop",
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
                    titole: "DC",
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
                    titole: "Sites",
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
@import "../assets/style/common.scss";

.c-footerTop {
    background-position: center;
    background-size: cover;

    &__nav {
        height: 400px;
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
    }

    &__img {
        height: 400px;
        width: 50%;
        object-fit: cover;
    }

}
</style>