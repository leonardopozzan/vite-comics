<template>
    <div class="card">
        <div class="img-box"><img :src="obj.thumb" alt=""></div>
        <div class="title">
            {{obj.series}}
        </div>
    </div>
</template>

<script>
    export default {
        dat(){
            return{

            }
        },
        props: ['obj']
    }
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;
@use '../assets/styles/partials/mixins' as *;
    .card{
        width: calc(100% / 6);
        padding: 1rem;
        
        .img-box{
            height: 150px;
            overflow: hidden;
            margin-bottom: 1rem;
        }
        .title{
            @include myText(0.9rem); 
        }
    }
</style>