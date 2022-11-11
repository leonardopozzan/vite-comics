<template>
    <nav class="nav-bar my-container">
        <div class="logo-img"><img src="/img/dc-logo.png" alt="logo"></div>
        <ul class="links">
            <li v-for="(section,i) in sections" :key="i" :class="{'active' : section.active}"><a :href="section.url">{{section.text}}</a></li>
        </ul>
    </nav>
</template>

<script>
import {sections} from '../data/data'
    export default {
        data(){
            return{
                sections: sections
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