<template>
    <AppHeader @onClickHeaderHamburgerButton="onClickHeaderHamburgerButton" />
    <AppNavigation v-if="isAppNavigation" @onClickHeaderCloseButton="onClickHeaderCloseButton"/>
    <LandingPage />
    <AppContactUs />
    <AppFooter />
</template>

<script>
import AppContactUs from './components/AppContactUs.vue';
import AppFooter from './components/AppFooter.vue';
import AppHeader from './components/AppHeader.vue';
import AppNavigation from './components/AppNavigation.vue'
import LandingPage from './views/LandingPage.vue';
export default {
    name: 'App',
    components: {
        AppHeader,
        AppNavigation,
        AppFooter,
        LandingPage,
        AppContactUs
},
    data(){
        return {
            isAppNavigation: false
        }
    },
    methods: {
        onClickHeaderHamburgerButton(){
            this.isAppNavigation = true
        },
        onClickHeaderCloseButton(){
            this.isAppNavigation = false
        }
    }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Rubik:wght@400;500&display=swap');
#app {
    font-family: 'Rubik', sans-serif;
    @apply
        relative
}
</style>