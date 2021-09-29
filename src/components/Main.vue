<template>
<div class="c-main">
    <div class="l-container">
        <h1>Content goes here</h1>
    </div>
</div>
</template>

<script>
export default {
    name: "Main",
    data: function() {
        return {
            
        }
    }
}
</script>

<style scoped lang="scss">
@import "../assets/style/variables.scss";
@import "../assets/style/common.scss";

.c-main {
    background-color: $gray-600;
    padding: 2rem 0;
    
    color: white;
}
</style>