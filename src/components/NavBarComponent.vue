<template>
    <nav class="nav-bar my-container">
        <div class="logo-img"><img src="../../public/img/dc-logo.png" alt="logo"></div>
        <ul class="links">
            <li v-for="(section,i) in sections" :key="i" :class="{'active' : section.active}"><a :href="section.url">{{section.text}}</a></li>
        </ul>
    </nav>
</template>

<script>
    export default {
        data(){
            return{
                sections: [
                    {
                        text: "Characters",
                        url: "#",
                        active: false,
                    },
                    {
                        text: "Comics",
                        url: "#",
                        active: true,
                    },
                    {
                        text: "Movies",
                        url: "#",
                        active: false,
                    },
                    {
                        text: "TV",
                        url: "#",
                        active: false,
                    },
                    {
                        text: "Games",
                        url: "#",
                        active: false,
                    },
                    {
                        text: "Collectibles",
                        url: "#",
                        active: false,
                    },
                    {
                        text: "Videos",
                        url: "#",
                        active: false,
                    },
                    {
                        text: "Fans",
                        url: "#",
                        active: false,
                    },
                    {
                        text: "News",
                        url: "#",
                        active: false,
                    },
                    {
                        text: "Shop",
                        url: "#",
                        active: false,
                    },
                ]
            }
        }
        
    }
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;
@use '../assets/styles/partials/mixins' as *;
    .nav-bar{
        height: 100px;
        @include dflex('between');
        .logo-img{
            width: 90px
        }
        .links{
            @include dflex();
            li{
                line-height: 97px;
                padding: 0 0.7rem;
                border-bottom: 3px solid transparent;
                transition: 0.3s;
                text-transform: uppercase;
                &.active,
                &:hover{
                    border-bottom: 3px solid $blue;
                    cursor: pointer;
                }
            }
        }
    }
</style>