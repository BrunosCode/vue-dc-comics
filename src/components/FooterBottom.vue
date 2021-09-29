<template>
<div class="c-footerBottom">
    <div class="l-container l-row l-row--spacebetween">
        <a class="c-btn c-ctaBtn c-footerBottom__btn">Sign-up Now!</a>

        <div class="l-row">
            <p>Folow now!</p>
            <ul class="c-footerBottom__iconsLinks h-listReset l-row">
                <li v-for="(link, i) in iconLinks" :key="i">
                    <a :href="link.url"
                    class="c-footerBottom__link c-link">
                        <img :src="require(`@/assets/images/${link.img}`)" :alt="link.text"
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
    name: "FooterBottom",
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
@import "../assets/style/common.scss";

.c-footerBottom {
    background-color: $gray-600;
    padding: 1rem;

}
</style>