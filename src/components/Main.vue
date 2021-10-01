<template>
<div class="c-main">
    <Hero hero-img="jumbotron.jpg"/>
    <Collection v-for="(collection, i) in collections" :key="i" :collection-data="collection"/>
    <ShopBanner :shop-icon-links="shopIconLinks"/>
</div>
</template>

<script>
import Hero from "./Hero.vue";
import Collection from "./Collection.vue";
import ShopBanner from "./ShopBanner.vue";
import dcComicsJson from "../data/dc-comics.json";

export default {
    name: "Main",
    components: {
        Hero,
        Collection,
        ShopBanner
    },
    data: function() {
        return {
            collections: {
                currentSeries: dcComicsJson
            },
            shopIconLinks: [
                {
                    text: "Digital Comics",
                    url: "#",
                    img: "buy-comics-digital-comics.png",
                },
                {
                    text: "DC Merchandise",
                    url: "#",
                    img: "buy-comics-merchandise.png",
                },
                {
                    text: "Subscription",
                    url: "#",
                    img: "buy-comics-subscriptions.png",
                },
                {
                    text: "Comic Shop Locator",
                    url: "#",
                    img: "buy-comics-shop-locator.png",
                },
                {
                    text: "DC Power Visa",
                    url: "#",
                    img: "buy-dc-power-visa.svg",
                },
            ]
        }
    }
}
</script>

<style scoped lang="scss">
@import "../assets/style/variables.scss";

.c-main {
    background-color: $gray-600;
    color: white;
}
</style>