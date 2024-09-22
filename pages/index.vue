<template>
    <div>
        <nav-bar />
        <home-header />
    </div>
</template>

<script>
import NavBar from '~/components/NavBar.vue';
import HomeHeader from '~/components/HomeHeader.vue';

    export default {
        name: 'index',
        components: {
            'nav-bar': NavBar,
            'home-header': HomeHeader,
        },
    }
</script>

<style scoped>

</style>