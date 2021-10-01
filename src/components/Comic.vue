<template>
<div class="c-comic l-col">
    <a href="#" class="c-btn">
        <div class="c-comic__squaredCover">
            <img :src="comicData.thumb"
            :alt="comicData.series" class="c-comic__squaredImg">
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
    &__squaredCover {
    padding-top: 100%;
    position: relative;
    overflow: hidden;

    }
    &__squaredImg {
            position: absolute;
            top: 0;
            right: 0;
            width: 100%;
            height: 100%;
            object-fit: cover;
            object-position: top center;
    }

    &__titole {
        margin-top: .5rem;
        text-transform: uppercase;
        font-size: .875rem;
    }
}
</style>