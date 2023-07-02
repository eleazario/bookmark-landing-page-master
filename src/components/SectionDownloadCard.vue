<template>
    <div class="sectionDownloadCard">
        <div class="sectionDownloadCardTop">
            <img :src="require(`../assets/images/logo-${browserName}.svg`)" alt="" class="browserLogo">
            <h3 class="cardTitle">Add to <span class="browserName">{{ browserName }}</span></h3>
            <p class="cardDescription">Minimum version {{ minVersion }}</p>
        </div>
        <img src="../assets/images/bg-dots.svg" alt="">
        <div class="sectionDownloadCardBottom">
            <BaseButton 
                :btn-text="'Add & Install Extension'"
                :btn-style="'primary'"
            />
        </div>
    </div>
</template>
<script>
import BaseButton from './BaseButton.vue';

export default {
    name: "SectionDownloadCard",
    components: { BaseButton },
    props: {
        browserName: String,
        minVersion: String
    }
}
</script>
<style scoped>
.sectionDownloadCard {
    @apply
        shadow-xl
        shadow-gray-200
        rounded-2xl
    }
    
.sectionDownloadCardTop {
    @apply
        py-8
        text-center
}

.browserLogo {
    @apply
        mx-auto
        mb-7
}

.sectionDownloadCardBottom {
    @apply
        p-6
}

.cardTitle {
    @apply
        text-xl
        text-gray-800
        font-medium
        mb-2
}

.browserName {
    @apply
        capitalize
}

.cardDescription {
    @apply
        text-sm
        text-gray-400
}
</style>