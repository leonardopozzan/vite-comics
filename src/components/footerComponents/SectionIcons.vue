<template>
    <section class="icons-wrap">
        <div class="icons">
            <div v-for="(link,i) in linksImage" :key="i" class="icon">
                <img :src="`img/${link.url}`" class="img-icon">
                <a href="#">{{link.text}}</a>
            </div>
        </div>
    </section>
</template>

<script>
import {linksImage} from '../../data/data'
    export default {
        data(){
            return{
                linksImage:linksImage
            }
        }
    }
</script>

<style lang="scss" scoped>
@use '../../assets/styles/partials/variables' as *;
@use '../../assets/styles/partials/mixins' as *;

    .icons-wrap{
        background-color: $blue;
        padding: 3rem 0;
        .icons{
            margin: auto;
            width: 80%;
            @include dflex();
        }
        
        .icon{
            @include dflex();
            width: calc(100% /5);
            padding-right: 1.5rem;
            .img-icon{
                width: 45px;
            }
            a{
                @include myText(0.9rem);
                padding-left: 0.8rem;
            }
        }
        .icon:nth-child(4) .img-icon{
            width: 25px;
        }
    }
</style>