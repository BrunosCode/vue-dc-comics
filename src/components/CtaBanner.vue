<template>
<div class="c-ctaBanner">
    <div class="l-container l-row l-row--spacebetween">
        <a class="c-btn c-cta c-ctaBanner__btn">Sign-up Now!</a>

        <div class="l-row">
            <p class="c-cta">Follow now!</p>
            <ul class="c-ctaBanner__iconsLinks h-listReset l-row">
                <li v-for="(link, i) in iconLinks" :key="i">
                    <a :href="link.url"
                    class="c-ctaBanner__link c-btn">
                        <img :src="require(`../assets/images/${link.img}`)" :alt="link.text"
                        class="c-footerBootom__icon">
                    </a>
                </li>
            </ul>
        </div>
    </div>
</div>
</template>

<script>
export default {
    name: "CtaBanner",
    data: function() {
        return {
            iconLinks: [
                {
                    text: "DC Facebook",
                    url: "#",
                    img: "footer-facebook.png",
                },
                {
                    text: "DC Twitter",
                    url: "#",
                    img: "footer-twitter.png",
                },
                {
                    text: "DC Youtube",
                    url: "#",
                    img: "footer-youtube.png",
                },
                {
                    text: "DC Pinterest",
                    url: "#",
                    img: "footer-pinterest.png",
                },
                {
                    text: "DC Periscope",
                    url: "#",
                    img: "footer-periscope.png",
                },
            ]
        }
    }
}
</script>

<style scoped lang="scss">
@import "../assets/style/variables.scss";

.c-ctaBanner {
    background-color: $gray-600;
    padding: 1rem;
    color: $primary;

    &__btn {
        padding: 1rem;
        border-color: $primary;
        color: white;
    }

    &__link {
        margin-left: 1rem;
    }
}
</style>