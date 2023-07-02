<template>
    <div class="sectionDownload">
        <SectionDownloadCard 
            :browser-name="'chrome'"
            :min-version="'62'"
        />
        <SectionDownloadCard 
            :browser-name="'firefox'"
            :min-version="'55'"
            class="mt-10 -mb-10"
        />
        <SectionDownloadCard 
            :browser-name="'opera'"
            :min-version="'46'"
            class="mt-20 -mb-20"
        />
    </div>
</template>
<script>
import SectionDownloadCard from './SectionDownloadCard.vue';

export default {
    name: "SectionDownload",
    components: { SectionDownloadCard }
}
</script>
<style scoped>
.sectionDownload {
    @apply
        relative
        flex
        flex-col
        lg:flex-row
        justify-center
        gap-16
        lg:gap-9
        px-12
        pt-4
}
</style>