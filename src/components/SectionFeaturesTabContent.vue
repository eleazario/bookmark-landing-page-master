<template>
    <div v-if="contentId===activeTab" class="tabContent">
        <div class="titleImageBox">
            <img :src="require(`../assets/images/${contentImage}`)" alt="" class="titleImage">
            <div class="titleImageShapeBox">
                <div class="titleImageShape"></div>
            </div>
        </div>
        <div class="tabContentDescriptionBox">
            <div class="tabContentTextBox">
                <h2>{{ contentTitle }}</h2>
                <p>{{ contentDescription }}</p>
            </div>
            <BaseButton
                :btn-text="'More Info'"
                :btn-style="'primary'"
                class="moreInfoButton"
            />
        </div>
    </div>
</template>
<script>
import BaseButton from './BaseButton.vue';

export default {
    name: "SectionFeaturesTabContent",
    components: { BaseButton },
    props: {
        contentId: Number,
        contentTitle: String,
        contentDescription: String,
        contentImage: String,
        activeTab: Number
    }
}
</script>
<style scoped>
.tabContent {
    @apply
        flex
        flex-col
        lg:flex-row
        justify-center
        lg:gap-20
}

.titleImageBox {
    @apply
        relative
        mb-20
        lg:mb-0
        lg:flex-auto
}

.titleImage {
    @apply
        sticky
        z-10
        px-7
        pt-2
        lg:ml-auto
}

.titleImageShapeBox {
    @apply
        absolute
        w-full
        h-full
        -bottom-10
        left-0
    }
    
.titleImageShape {
    @apply
        absolute
        bottom-0
        left-0
        bg-Soft-Blue
        h-full
        lg:h-[87%]
        w-4/5
        rounded-r-full
}

.tabContentDescriptionBox {
    @apply
        flex
        flex-col
        justify-center
        lg:w-[28rem]
        lg:mr-40
        flex-auto
}

.tabContentTextBox {
    @apply
        text-center
        lg:text-start
        px-8
        lg:px-0
        mx-auto
        lg:mx-0
        mb-9
}

.tabContentTextBox > h2 {
    @apply
        text-2xl
        lg:text-[1.925rem]
        text-gray-800
        font-medium
        mb-3
        lg:mb-6
}

.tabContentTextBox > p {
    @apply
        text-base
        lg:text-lg
        text-gray-400
}

.moreInfoButton {
    @apply
        hidden
        lg:block
        w-28
}
</style>