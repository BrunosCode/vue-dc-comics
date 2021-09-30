<template>
<div class="c-comic l-col">
    <img :src="comicData.thumb"
    :alt="comicData.series" class="c-comic__img">
    <p class="c-comic__titole">{{comicData.series}}</p>
</div>
</template>

<script>
export default {
    name: "Comic",
    props: {
        comicData: Object
    },
}

</script>

<style scoped lang="scss">
@import "../assets/style/variables.scss";

.c-comic {
    &__img {
        width: 100%;
    }
    &__titole {
        margin-top: .5rem;
        text-transform: uppercase;
    }
}
</style>