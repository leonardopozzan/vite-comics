<template>
    <div class="flip-card">
        <div class="flip-card-inner">
            <div class="flip-card-front">
                <div class="img-box"><img :src="obj.thumb" alt=""></div>
                <span class="title">{{obj.series}}</span>
            </div>
            <div class="flip-card-back">
                <div class="img-box"><img :src="obj.thumb" alt=""></div>
                <span class="title">{{obj.price}}</span>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        dat(){
            return{

            }
        },
        props: ['obj', 'index']
    }
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;
@use '../assets/styles/partials/mixins' as *;
    .flip-card{
        width: calc(100% / 6);
        height: 285px;
        padding: 0.5rem;
        background-color: white;
        border: 4px solid $dark-dc;
        perspective: 1000px;
        .flip-card-inner{
            position: relative;
            width: 100%;
            height: 100%;
            text-align: center;
            transition: transform 0.6s;
            transform-style: preserve-3d;
            .flip-card-front, .flip-card-back{
                position: absolute;
                width: 100%;
                height: 100%;
                -webkit-backface-visibility: hidden;
                backface-visibility: hidden;
                
            }
            .flip-card-back{
                transform: rotateY(180deg);
            }
        }
        &:hover .flip-card-inner{
            transform: rotateY(180deg);
        }
        .title{
            @include myText(0.9rem);
            color: black; 
        }
        .img-box{
            height: 200px;
            overflow: hidden;
            margin-bottom: 0.5rem;
        }
        
    }
</style>