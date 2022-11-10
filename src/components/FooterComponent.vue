<template>
    <footer>
        <SectionIcons />
    </footer>
</template>

<script>
import SectionIcons from './footerComponents/SectionIcons.vue';

    export default {
    components: { SectionIcons }
}
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;
@use '../assets/styles/partials/mixins' as *;

</style>