<template>
    <div class="navigation">
        <nuxt-link to="/" class="big" :style="'color:' + linkColor + ''">home</nuxt-link>
        <nuxt-link to="/about" class="big" :style="'color:' + linkColor + ''">about</nuxt-link>
        <nuxt-link to="/media" class="big" :style="'color:' + linkColor + ''">media</nuxt-link>
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
        props: ['linkColor']
    }
</script>

<style scoped>



</style>
