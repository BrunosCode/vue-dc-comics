<template>
<div class="c-comic l-col">
    <a href="#" class="c-btn">
        <div class="l-square">
            <img :src="comicData.thumb"
            :alt="comicData.series" class="l-square__img c-comic__img">
        </div>
        <p class="c-comic__titole">{{comicData.series}}</p>
    </a>
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
        position: absolute;
        top: 0;
        right: 0;
        width: 100%;
        object-fit: contain;
        object-position: center;
    }
    &__titole {
        margin-top: .5rem;
        text-transform: uppercase;
        font-size: .875rem;
    }
}
</style>