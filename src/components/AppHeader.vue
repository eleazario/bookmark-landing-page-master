<template>
    <header>
        <a href="" class="appLogoHeader">
            <img src="../assets/images/logo-bookmark.svg" alt="">
        </a>
        <button @click="clickHeaderHamburgerButton" class="hamburgerIconButton">
            <img src="../assets/images/icon-hamburger.svg" alt="">
        </button>
        <nav>
            <ul>
                <li class="navItem"><a href="">Features</a></li>
                <li class="navItem"><a href="">Pricing</a></li>
                <li class="navItem"><a href="">Contact</a></li>
                <li><a href="">
                    <BaseButton 
                        :btn-text="'LOGIN'"
                        :btn-style="'tertiary'"
                        class="buttonLogin"
                    />
                </a></li>
            </ul>
        </nav>
    </header>
</template>
<script>
import BaseButton from './BaseButton.vue';
export default {
    name: 'AppHeader',
    components: {
        BaseButton
    },
    methods: {
        clickHeaderHamburgerButton(){
            this.$emit('onClickHeaderHamburgerButton')
        }
    }
}
</script>
<style scoped>
header {
    @apply
        sticky
        top-0
        flex
        px-8
        py-10
        lg:px-[10.5rem]
        items-center
        bg-white
        z-20
}

.hamburgerIconButton {
    @apply
        ml-auto
        lg:hidden
}

nav {
    @apply
        hidden
        lg:flex
        ml-auto
}

nav > ul {
    @apply
        flex
}

.navItem {
    @apply
        flex
        items-center
        text-[0.825rem]
        uppercase
        ml-11
        tracking-widest
        hover:text-Soft-Red
}

.buttonLogin {
    @apply
        ml-12
        w-28
        py-2
        text-xs
        tracking-widest
    }
    
</style>