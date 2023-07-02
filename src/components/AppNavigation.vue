<template>
    <aside id="app-navigation">
        <div class="appNavigationHeader">
            <a href="" class="appLogoHeader">
                <img src="../assets/images/logo-bookmark-white.svg" alt="">
            </a>
            <button @click="clickHeaderCloseButton" class="hamburgerIconButton">
                <img src="../assets/images/icon-close.svg" alt="">
            </button>
        </div>
        <nav>
            <ul>
                <li class="navItem"><a href="">Features</a></li>
                <li class="navItem"><a href="">Pricing</a></li>
                <li class="navItem"><a href="">Contact</a></li>
            </ul>
            <BaseButton 
                :btn-style="'outline'"
                :btn-text="'Login'"
                class="mt-6"
            />
        </nav>
        <ul class="socialMediaBox">
            <li><a href=""><img src="../assets/images/icon-facebook.svg" alt=""></a></li>
            <li><a href=""><img src="../assets/images/icon-twitter.svg" alt=""></a></li>
        </ul>
    </aside>
</template>
<script>
import BaseButton from './BaseButton.vue'
export default {
    name: 'AppNavigation',
    components: {
        BaseButton
    },
    methods: {
        clickHeaderCloseButton(){
            this.$emit('onClickHeaderCloseButton')
        }
    },
}
</script>
<style scoped>
#app-navigation {
    @apply
        fixed
        top-0
        z-20
        flex
        flex-col
        px-8
        pb-12
        h-full
        w-full
        bg-Very-Dark-Blue
        bg-opacity-95
}

.appNavigationHeader {
    @apply
        flex
        py-10
        border-b-2
        border-Grayish-Blue
        border-opacity-20
}

.hamburgerIconButton {
    @apply
        ml-auto
}

.navItem {
    @apply
        flex
        border-b-2
        border-Grayish-Blue
        border-opacity-20
}

.navItem > a {
    @apply
        flex-auto
        py-4
        text-gray-200
        text-center
        text-xl
        uppercase
        tracking-widest
}

.socialMediaBox {
    @apply
        flex
        justify-center
        content-end
        gap-10
        mt-auto
}

.socialMediaBox > li, .socialMediaBox > li > a {
    @apply
        flex
        content-center
}

.socialMediaBox > li > a > img {
    @apply
        object-contain
}

</style>