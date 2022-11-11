<template>
    <div class="jumbo">
        <div class="my-container">
            <div class="title">
                current series
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        
    }
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;
@use '../assets/styles/partials/mixins' as *;
    .jumbo{
        background-image: url('/img/jumbotron.jpg');
        background-size: cover;
        height: 400px;
        position: relative;
        .title{
            position: absolute;
            bottom: 0px; 
            transform: translate( 0, 50%);
            padding: 0.8rem;
            background-color: $blue;
            @include myText(1rem,bold);
        }
    }
</style>