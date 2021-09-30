<template>
<div class="c-hero">
    <img src="../assets/images/jumbotron.jpg" alt="Jumbotron"
    class="c-hero__img">
</div>
</template>

<script>
export default {
    name: "Hero",
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