<template>
    <section class="icons">
        <div v-for="(link,i) in linksImage" :kei="i" class="my-container icon">
            <img :src="getImagePath(`../../assets/img/${link.url}`)" class="img-icon">
            <a href="#">{{link.text}}</a>
        </div>
    </section>
</template>

<script>
    export default {
        data(){
            return{
                linksImage : [
                    {
                        text: 'digital comics',
                        url: 'buy-comics-digital-comics.png'
                    },
                    {
                        text: 'dc merchandise',
                        url: 'buy-comics-merchandise.png'
                    },
                    {
                        text: 'subscription',
                        url: 'buy-comics-subscriptions.png'
                    },
                    {
                        text: 'comic shop locator',
                        url: 'buy-comics-shop-locator.png'
                    },
                    {
                        text: 'dc power visa',
                        url: 'buy-dc-power-visa.svg'
                    }
                ]
            }
        },
        methods: {
            getImagePath(imgPath){
                return new URL(imgPath, import.meta.url).href;
            }
        }
    }
</script>

<style lang="scss" scoped>
@use '../../assets/styles/partials/variables' as *;
@use '../../assets/styles/partials/mixins' as *;

    .icons{
        background-color: $blue;
        @include dflex();
        padding: 1rem;
        .icon{
            @include dflex();
            .img-icon{
                width: 45px;
                margin-right: 10px;
            }
            a{
                color: $white;
                font-size: 1.1rem;
                text-transform: uppercase;
            }
        }
    }
</style>