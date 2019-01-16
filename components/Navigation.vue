<template>
    <div class="navigation">
        <nuxt-link to="/" class="big">home</nuxt-link>
        <nuxt-link to="/about" class="big">about</nuxt-link>
        <nuxt-link to="/media" class="big">media</nuxt-link>
    </div>
</template>

<script>

    export default {
        name: 'Navigation',
        components: {

        },
        data() {
            return {}
        }
    }
</script>

<style scoped>
.navigation {
    padding-top: 26px;
    display: flex;
    height: 30px;
    /*padding-left: 80px;*/
}

.navigation a {
    margin-left: 20px;
    font-size: 18px;
}


</style>
