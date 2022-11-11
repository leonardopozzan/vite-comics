<template>
    <HeaderComponent />
    <MainComponent />
    <FooterComponent />
</template>

<script>
import FooterComponent from './components/FooterComponent.vue';
import HeaderComponent from './components/HeaderComponent.vue';
import JumboComponent from './components/JumboComponent.vue';
import MainComponent from './components/MainComponent.vue';

export default {
    components: { HeaderComponent, MainComponent, FooterComponent, JumboComponent }
}
</script>

<style lang="scss">
@use './assets/styles/partials/mixins' as *;
@use './assets/styles/partials/variables' as *;

</style>