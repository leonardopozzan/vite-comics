<template>
    <header>
        <NavBarComponent />
    </header>
</template>

<script>
import NavBarComponent from './NavBarComponent.vue';

export default {
    data() {
    },
    components: { NavBarComponent }
}
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;
@use '../assets/styles/partials/mixins' as *;

    header {
        background-color: $white;
    }

</style>