<template>
    <main>
        <div class="my-container">
            <h1> -->Content goes Here&lt;-- </h1>
        </div>
    </main>
</template>

<script>
    export default {
        
    }
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;
@use '../assets/styles/partials/mixins' as *;

    main{
        background-color: $black;
        height: 20vh;
        @include dflex();
        h1{
            color: $white;
        }
    }
</style>