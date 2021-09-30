<template>
<div class="c-header">
    <div class="l-container l-row l-row--spacebetween">
        <a href="#">
            <img  class="c-header__logo" src="../assets/images/dc-logo.png" alt="DC Logo">
        </a>
        <nav class="c-header__nav">
            <ul class="l-row h-listReset">
                <li v-for="(link, i) in menu" :key="i"  class="h-align--stretch">
                    <a :href="link.url" :class="{'active': link.current}"
                    class="c-header__link c-link">
                        {{link.text}}
                    </a>
                </li>
            </ul>
        </nav>
    </div>
</div>
</template>

<script>
export default {
    name: "Header",
    data: function() {
        return {
            menu: [
                {
                    text: "Characters",
                    url: "#",
                    current: false,
                },
                {
                    text: "Comics",
                    url: "#",
                    current: true,
                },
                {
                    text: "Movies",
                    url: "#",
                    current: false,
                },
                {
                    text: "TV",
                    url: "#",
                    current: false,
                },
                {
                    text: "Games",
                    url: "#",
                    current: false,
                },
                {
                    text: "Collectibles",
                    url: "#",
                    current: false,
                },
                {
                    text: "Videos",
                    url: "#",
                    current: false,
                },
                {
                    text: "Fans",
                    url: "#",
                    current: false,
                },
                {
                    text: "News",
                    url: "#",
                    current: false,
                },
                {
                    text: "Shop",
                    url: "#",
                    current: false,
                },
            ]
        }
    }
}
</script>

<style scoped lang="scss">
@import "../assets/style/variables.scss";

.c-header {
    &__logo {
        height: 5rem;
    }

    &__nav {
        height: 7rem;
    }

    &__link {
        padding: 0 .5rem;
        color: $gray-400;
        font-weight: 700;
        text-transform: uppercase;
        display: inline-block;
        line-height: 7rem;
        
        &.active {
            color: $primary;
            box-shadow: inset 0 -.3rem $primary;
        }

        &:hover {
            background-color: $gray-300;
            color: white;
        }
    }
}
</style>