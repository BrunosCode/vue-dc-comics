<template>
<div class="c-collection l-container">
    <h2 class="c-collection__titole">Current Series</h2>
    <div class="c-collection__comics">
        <Comic v-for="(comic, i) in collectionData" :key="i" :comic-data="comic"/>
    </div>
    <button class="c-btn c-collection__btn">Load More</button>
</div>
</template>

<script>
import Comic from './Comic.vue';

export default {
    name: "Collection",
    components: {
        Comic
    },
    props: {
        collectionData:  Array,
    },
}
</script>

<style scoped lang="scss">
@import "../assets/style/variables.scss";

.c-collection {
    margin-top: 1rem;
    position: relative;
    top: -2.5rem;

    &__comics {
        display: grid;
        grid-template-columns: repeat(6, 1fr);
        grid-template-rows: repeat(2, 1fr);
        column-gap: 1rem;
        row-gap: 1rem;
        margin: 2rem .5rem;
    }

    &__titole {
        display: inline-block;
        font-weight: 700;
        text-transform: uppercase;
        padding: .5rem;
        background-color: $primary;
    }

    &__btn {
        display: block;
        margin: 0 auto;
        font-weight: 700;
        text-transform: uppercase;
        padding: .5rem 2rem;
        background-color: $primary;
        color: white;
    }
}

</style>