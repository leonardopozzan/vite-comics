<template>
    <div class="my-container">
        <div class="cards">
            <CardComponent v-for="(item,i) in ComicsImage" :key="i" :obj="item"/>
        </div>
    </div>
</template>

<script>
import CardComponent from './CardComponent.vue';
import { mainComics } from '../data/data';

    export default {
        data(){
            return{
                ComicsImage: mainComics
            }
        },
    components: { CardComponent }
}
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;
@use '../assets/styles/partials/mixins' as *;
    .cards{
        display: flex;
        flex-wrap: wrap;
        margin: 0 -1rem;
    }
</style>