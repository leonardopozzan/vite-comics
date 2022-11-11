<template>
    <section class="contacts-wrap">
        <div class="my-container contacts">
            <button>sign-up now</button>
            <div class="social">
                <span>follow us</span>
                <a href="#"><img src="/img/footer-facebook.png" alt=""></a>
                <a href="#"><img src="/img/footer-twitter.png" alt=""></a>
                <a href="#"><img src="/img/footer-youtube.png" alt=""></a>
                <a href="#"><img src="/img/footer-pinterest.png" alt=""></a>
                <a href="#"><img src="/img/footer-periscope.png" alt=""></a>
            </div>
        </div>
    </section>
</template>

<script>
    export default {
        data(){
            return{
                
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
                &>*{
                    margin-right: 0.7rem
                }
                @include dflex();
                span{
                    text-transform: uppercase;
                    color: $blue;
                    font-weight: bold;
                    font-size: 1.2rem;
                }
                img:hover{
                    filter: brightness(0) invert(1);
                    cursor: pointer;
                }
            }
        }
        button{
            padding: 0.8rem;
            text-transform: uppercase;
            background-color: transparent;
            color: $white;
            border: 2px solid $blue;
            cursor: pointer;
            &:hover{
                background-color: $white;
                color: $blue;
            }
        }
    }
</style>