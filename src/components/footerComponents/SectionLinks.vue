<template>
    <section class="links-footer">
        <div class="my-container links-wrap">
            <div class="links">
                <div class="link">
                    <span class="title">dc comics</span>
                    <ul>
                        <li v-for="(link, i) in linksComics" :key="i"><a href="link.url">{{link.text}}</a></li>
                    </ul>
                    <span class="title">shop</span>
                    <ul>
                        <li v-for="(link, i) in linksShop" :key="i"><a href="link.url">{{link.text}}</a></li>
                    </ul>
                </div>
                <div class="link">
                    <span class="title">dc</span>
                    <ul>
                        <li v-for="(link, i) in linksDc" :key="i"><a href="link.url">{{link.text}}</a></li>
                    </ul>
                </div>
                <div class="link">
                    <span class="title">sites</span>
                    <ul>
                        <li v-for="(link, i) in linksSites" :key="i"><a href="link.url">{{link.text}}</a></li>
                    </ul>
                </div>
            </div>
            <div class="img-box"><img src="/img/dc-logo-bg.png" alt=""></div>
        </div>
    </section>
</template>

<script>
import {linksComics,linksShop,linksDc,linksSites} from '../../data/data'
    export default {
        data(){
            return{
                linksComics : linksComics,
                linksShop: linksShop,
                linksDc: linksDc,
                linksSites: linksSites
            }
        }
    }
</script>

<style lang="scss" scoped>
@use '../../assets/styles/partials/variables' as *;
@use '../../assets/styles/partials/mixins' as *;
    .links-footer{
        background-image: url('/img/footer-bg.jpg');
        background-size: cover;
        background-position: center;        
        .links-wrap{
            @include dflex('between');
            height: 400px;
            overflow: hidden;
                .links{
                display: flex;
                .link{
                    padding: 1rem 1rem 1rem 0;
                    .title{
                        @include myText(1.5rem,bold);
                        display: inline-block;
                        padding: 0.8rem 0;
                    }
                    li{
                        padding: 0.1rem 0;
                    }
                    a{
                        color: grey;

                        &:hover{
                            color: $white;
                        }
                    }
                }
            }
        }
    }
</style>