<template>
    <section class="contacts-wrap">
        <div class="my-container contacts">
            <button>sign-up now</button>
            <div class="social">
                <span>follow us</span>
                <!-- <a href="#" v-for="(path, i) in social" :key="i"><img :src="`/img/${path}`" alt=""></a> -->
                <ul>
                    <li><a href="#"><i class="fa-brands fa-facebook"></i></a></li> 
                    <li><a href="#"><i class="fa-brands fa-twitter"></i></a></li> 
                    <li><a href="#"><i class="fa-brands fa-youtube"></i></a></li>  
                    <li><a href="#"><i class="fa-brands fa-pinterest"></i></a></li>  
                    <li><a href="#"><i class="fa-brands fa-periscope"></i></a></li> 
                </ul>
            </div>
        </div>
    </section>
</template>

<script>
    export default {
        data(){
            return{
                social : [
                'footer-facebook.png',
                'footer-twitter.png',
                'footer-youtube.png',
                'footer-pinterest.png',
                'footer-periscope.png'
                ]
            }
        }
    }
</script>

<style lang="scss" scoped>
@use '../../assets/styles/partials/variables' as *;
@use '../../assets/styles/partials/mixins' as *;

    .contacts-wrap{
        background-color: $dark-grey;
        .contacts{
            padding: 1.2rem 0;
            @include dflex('between');
            .social{
                @include dflex();
                span{
                    margin-right: 0.7rem;
                    @include myText(1.2rem,bold);
                    color: $blue;
                }
                img:hover{
                    filter: brightness(0) invert(1);
                    cursor: pointer;
                }
                ul{
                    position: relative;
                    display: flex;
                    li{
                        position: relative;
                        margin: 0 0.5rem;
                        cursor: pointer;
                        a{
                            font-size: 2.5em;
                            color: #222;
                        }
                        &::before{
                            font-family: "FontAwesome";
                            font: var(--fa-font-brands);
                            position: absolute;
                            top: 0; left: 0;
                            font-size: 2.5em;
                            height: 0;
                            overflow: hidden;
                            transition: 0.5s ease-in-out;
                        }
                        &:first-child::before{
                            content: '\f09a';
                            color: #001eb4;
                            border-bottom: 4px solid #001eb4;
                        }
                        &:nth-child(2)::before{
                            content: "\f099";
                            color: #1DA1F2;
                            border-bottom: 4px solid #1DA1F2;
                        }
                        &:nth-child(3)::before{
                            content: "\f167";
                            color: red;
                            border-bottom: 4px solid red;
                        }
                        &:nth-child(4)::before{
                            content: "\f0d2";
                            background-image: linear-gradient(45deg,#f09433 0%, #e6883c 25%, #dc2743 50%, #cc2366 75%, #bc1888 100%);
                            -webkit-background-clip: text;
                            -webkit-text-fill-color: transparent;
                            border-bottom: 4px solid #dc2743;
                        }
                        &:nth-child(5)::before{
                            content: "\f3da";
                            color: white;
                            border-bottom: 4px solid white;
                        }
                        &:hover::before{
                            height: 100%;
                        }
                    }
                }
            }
        }
        button{
            padding: 0.8rem;
            @include myText();
            background-color: transparent;
            border: 2px solid $blue;
            cursor: pointer;
            &:hover{
                background-color: $white;
                color: $blue;
            }
        }
    }
</style>