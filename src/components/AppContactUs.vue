<template>
    <div id="contactUs">
        <div class="contactUsBox">
            <h4>35.000+ already joined</h4>
            <h2>Stay up-to-date with what we're doing</h2>
            <form @submit.prevent="submitEmail" novalidate >
                <div :class="['lg:flex-auto', {'bg-Soft-Red rounded-md': inputError}]">
                    <div :class="['inputBox', {'inputError': inputError}]">
                        <input v-model="emailAddress" type="email" name="email" id="email" placeholder="Enter your email address">
                        <img v-if="inputError" src="../assets/images/icon-error.svg" alt="">
                    </div>
                    <div v-if="inputError" class="errorMessage">Whoops, make sure it's an email</div>
                </div>
                <div>
                    <BaseButton 
                        :btn-text="'Contact Us'"
                        :btn-style="'tertiary'"
                        class="submitButton"
                    />
                </div>
            </form>
        </div>
    </div>
</template>
<script>
import BaseButton from './BaseButton.vue';

export default {
    name: "AppContactUs",
    components: { BaseButton },
    data() {
        return {
            emailAddress: '',
            inputError: false
        }
    },

    methods: {
        submitEmail(){
            if(this.validateEmail())
                this.inputError = false
            else
                this.inputError = true
        },

        validateEmail(){
            const validRegex = /^([A-Za-z0-9_\-.])+@([A-Za-z0-9_\-.])+.([A-Za-z]{2,4})$/
            if (this.emailAddress.match(validRegex))
                return true
            return false
        }
    }
}
</script>
<style scoped>
#contactUs {
    @apply
        bg-Soft-Blue
        text-white
        text-center
        px-8
        pt-[4.5rem]
        pb-14
}

.contactUsBox {
    @apply
        mx-auto
        lg:w-[27.5rem]
}

form {
    @apply
        flex
        flex-col
        lg:flex-row
        lg:gap-4
}

h4 {
    @apply
        text-xs
        uppercase
        tracking-[0.4em]
        mb-3
}

h2 {
    @apply
        text-2xl
        mb-7
        leading-tight
}

.inputBox {
    @apply
        flex
        bg-white
        rounded-md
        border-2
        border-white

}

.inputBox > input {
    @apply
        text-sm
        outline-none
        bg-transparent
        w-full
        text-slate-950
        placeholder:text-slate-300
        py-3
        px-5
}

.inputBox > img {
    @apply
        mr-3
        object-contain
}

.inputError {
    @apply
        border-Soft-Red
}

.errorMessage {
    @apply
        text-slate-200
        text-[0.65rem]
        text-start
        italic
        rounded-b-md
        border-Soft-Red
        border-b-2
        px-3
}

.submitButton {
    @apply
    mb-1
    mt-4
    lg:m-0
    lg:w-32
}

</style>