<template>
<div class="c-comic l-col">
    <img src="https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/AV1976_01_300-001_HD_5f738f6e39ddd7.18205602.jpg?itok=VgdYdJ01"
    :alt="comicData" class="c-comic__img">
    <p class="c-comic__titole">titolo</p>
</div>
</template>

<script>
export default {
    name: "Comic",
    prop: {
        comicData: Object
    },
}

</script>

<style scoped lang="scss">
@import "../assets/style/variables.scss";

.c-comic {
    width: calc((100% / 6) - 1rem);
}
</style>