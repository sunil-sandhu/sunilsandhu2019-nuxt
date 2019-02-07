<template>
    <div>
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
        },
        props: ['linkColor', 'navBackgroundColor']
    }
</script>

<style scoped>



</style>
