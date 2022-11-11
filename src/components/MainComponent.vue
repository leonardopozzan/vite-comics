<template>
    <main>
        <JumboComponent />
        <div class="inner-main">
            <CardsComponent />
            <ButtonComponent />
        </div>
    </main>
</template>

<script>
import JumboComponent from './JumboComponent.vue';
import CardsComponent from './CardsComponent.vue'
import ButtonComponent from './ButtonComponent.vue';
    export default {
    components: { JumboComponent, CardsComponent, ButtonComponent }
}
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;
@use '../assets/styles/partials/mixins' as *;

main{
    background-color: $dark-dc;
    .inner-main{
        padding: 2rem 0;
    }
}
</style>