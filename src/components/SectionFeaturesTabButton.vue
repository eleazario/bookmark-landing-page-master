<template>
    <button @click="featuresTabButtonClick(btnId)" class="featuresTabButton">
        {{ btnText }}
        <div :class="['line',{'activeLine':btnId===activeTab}]"><div></div></div>
    </button>
</template>
<script>
export default {
    name: 'SectionFeaturesTabButton',
    props: {
        btnId: Number,
        btnText: String,
        activeTab: Number
    },
    methods: {
        featuresTabButtonClick(btnId){
            this.$emit('onFeaturesTabButtonClick', btnId)
        }
    }
}
</script>
<style scoped>
.featuresTabButton {
    @apply
        relative
        w-full
        lg:w-64
        py-4
        lg:py-7
        border-b-2
        border-gray-200
        text-center
        lg:text-lg
        hover:text-Soft-Red
}

.line {
    @apply
        absolute
        bottom-0
        w-0
        transition-[width]
}
    
.line > div {
    @apply
        h-1
        mx-auto
        bg-Soft-Red
        transition-[width]
}

.activeLine {
    @apply
        w-full
}
.activeLine > div {
    @apply
        w-36
        lg:w-full
}

</style>