<template>
    <footer>
        <SectionIcons />
        <SectionLinks />
        <SectionSocial />
    </footer>
</template>

<script>
import SectionIcons from './footerComponents/SectionIcons.vue';
import SectionLinks from './footerComponents/SectionLinks.vue';
import SectionSocial from './footerComponents/SectionSocial.vue';

    export default {
    components: { SectionIcons, SectionLinks, SectionSocial }
}
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;
@use '../assets/styles/partials/mixins' as *;

</style>