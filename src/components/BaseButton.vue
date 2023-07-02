<template>
    <button
        :class="[
            {'btnPrimary': btnStyle === 'primary'},
            {'btnSecondary': btnStyle === 'secondary'},
            {'btnTertiary': btnStyle === 'tertiary'},
            {'btnOutline': btnStyle === 'outline'},
        ]"
    >
        {{ btnText }}
    </button>
</template>
<script>
export default {
    name: 'BaseButton',
    props: {
        btnStyle: {
            type: String,
            default: 'primary',
            validator(value){
                return ['primary', 'secondary', 'tertiary', 'outline'].includes(value)
            }
        },
        btnText: String
    }
}
</script>
<style scoped>
button {
    @apply
        w-full
        text-sm
        rounded-md
        border-2
        py-3
        shadow-lg
        transition-colors
}

.btnPrimary {
    @apply
        text-white
        bg-Soft-Blue
        border-Soft-Blue
        hover:text-Soft-Blue
        hover:bg-white
}
    
.btnSecondary {
    @apply
        text-gray-700
        bg-gray-100
        border-gray-100
        hover:bg-white
        hover:border-gray-700
}

.btnTertiary {
    @apply
        text-white
        bg-Soft-Red
        border-Soft-Red
        hover:text-Soft-Red
        hover:bg-white
}

.btnOutline {
    @apply
        text-white 
        border-white
        bg-transparent 
        uppercase 
        tracking-widest 
        text-lg
        py-2
}
</style>