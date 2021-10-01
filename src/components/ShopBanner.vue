<template>
<div class="c-banner">
    <div class="l-container">
        <ul class="c-banner__list l-row l-row--spacebetween h-listReset">
            <li v-for="(link, i) in shopIconLinks" :key="i">
                <a :href="link.url"
                class="c-banner__link c-btn l-row">
                    <img :src="require(`../assets/images/${link.img}`)" :alt="link.text"
                    class="c-banner__icon">
                    <span class="c-banner__text">{{link.text}}</span>
                </a>
            </li>
        </ul>
    </div>
</div>
</template>

<script>
export default {
    name: "ShopBanner",
    props: {
        shopIconLinks: Array
    }
}
</script>

<style scoped lang="scss">
@import "../assets/style/variables.scss";

.c-banner {
    padding: 2rem 0;
    background-color: $primary;

    &__list {
        padding: 0 1rem;
    }

    &__link {
        color: white;
        text-transform: uppercase;
    }

    &__icon {
        height: 2.5rem;
        vertical-align: middle;
        margin-right: .5rem;
    }
}
</style>