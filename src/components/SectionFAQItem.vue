<template>
    <div class="faqItem">
        <button @click="faqQuestionClick" class="faqQuestionBox">
            <h3 class="faqQuestion">{{ itemQuestion }}</h3>
            <svg :class="['dropDownIcon', {'dropDownIconActive': showAnswer}]" xmlns="http://www.w3.org/2000/svg" width="18" height="12"><path fill="none" stroke="#5267DF" stroke-width="3" d="M1 1l8 8 8-8"/></svg>
        </button>
        <p v-if="showAnswer" class="faqAnswer">{{ itemAnswer }}</p>
    </div>
</template>
<script>
export default {
    name: 'SectionFAQitem',
    props: {
        itemQuestion: String,
        itemAnswer: String,
    },
    data(){
        return {
            showAnswer: false
        }
    },
    methods: {
        faqQuestionClick(){
            this.showAnswer = !this.showAnswer
        }
    }
}
</script>
<style scoped>
.faqItem {
    @apply
        border-b-2
        border-gray-200
        lg:pr-6
}
.faqQuestionBox {
    @apply
        flex
        w-full
        py-4
}

.faqQuestionBox:hover > .faqQuestion {
    @apply
        text-Soft-Red
}

.faqQuestion {
    @apply
        text-[0.93rem]
        lg:text-lg
        text-gray-800
}

.dropDownIcon {
    @apply
        self-center
        ml-auto
        transition-[transform]
}

.dropDownIconActive {
    @apply
        -scale-y-100
}

.dropDownIconActive > path {
    @apply
        stroke-Soft-Red
}

.faqAnswer {
    @apply
        text-slate-500
        text-[0.93rem]
        lg:text-lg
        leading-7
        lg:leading-9
        pt-4
        pb-7
}

</style>