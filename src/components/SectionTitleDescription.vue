<template>
    <div class="sectionTextBox">
        <h2>{{ sectionTitle }}</h2>
        <p>{{ sectionDescription }}</p>
    </div>
</template>
<script>
export default {
    name: 'SectionTitleDescription',
    props: {
        sectionTitle: String,
        sectionDescription: String
    }
}
</script>
<style scoped>
.sectionTextBox {
    @apply
        text-center
        px-8
        lg:w-[37rem]
        mx-auto
        mb-9
        lg:mb-14
}

.sectionTextBox > h2 {
    @apply
        text-2xl
        lg:text-[2rem]
        text-gray-800
        font-medium
        mb-3
        lg:mb-6
}

.sectionTextBox > p {
    @apply
        text-base
        lg:text-lg
        text-gray-400
}
</style>