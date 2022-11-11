<template>
    <div class="btn">
        <button>load more</button>
    </div>
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
@use '../assets/styles/partials/variables' as *;
@use '../assets/styles/partials/mixins' as *;
.btn{
    text-align: center;
    button{
        background-color: $blue;
        padding: 0.5rem 2.5rem;
        color: $white;
        font-size: 1.1rem;
        text-transform: uppercase;
        font-weight: bold;
    }
}
</style>