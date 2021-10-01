<template>
<div class="c-hero">
    <img :src="require(`../assets/images/${heroImg}`)" alt="Jumbotron"
    class="c-hero__img">
</div>
</template>

<script>
export default {
    name: "Hero",
    props: {
        heroImg: String
    }
}
</script>

<style scoped lang="scss">
@import "../assets/style/variables.scss";

.c-hero {
    
    &__img {
        height: 400px;
        width: 100%;
        object-fit: cover;
        object-position: top center;
    }
}
</style>