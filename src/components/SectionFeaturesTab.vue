<template>
    <div>
        <div class="buttonTabBox">
            <SectionFeaturesTabButton
                :btn-id="0"
                :btn-text="'Simple Bookmarking'"
                :active-tab="activeTab"
                @onFeaturesTabButtonClick="onFeaturesTabButtonClick"
                class="border-t-2 border-gray-200 lg:border-t-0"
            />
            <SectionFeaturesTabButton
                :btn-id="1"
                :btn-text="'Speedy Searching'"
                :active-tab="activeTab"
                @onFeaturesTabButtonClick="onFeaturesTabButtonClick"
            />
            <SectionFeaturesTabButton
                :btn-id="2"
                :btn-text="'Easy Sharing'"
                :active-tab="activeTab"
                @onFeaturesTabButtonClick="onFeaturesTabButtonClick"
            />
        </div>
        <SectionFeaturesTabContent
            :content-id="0"
            :content-title="'Bookmark in one click'"
            :content-description="'Orginize your bookmarks however you like. Our simple drag-and-drop interface gives you complete control over how you manage your favourite sites.'"
            :content-image="'illustration-features-tab-1.svg'"
            :active-tab="activeTab"
        />
        <SectionFeaturesTabContent
            :content-id="1"
            :content-title="'Intellligent search'"
            :content-description="'Our powerfull searh feature will help your find saved sites in no time at all. No need to trawl through all of your bookmarks.'"
            :content-image="'illustration-features-tab-2.svg'"
            :active-tab="activeTab"
        />
        <SectionFeaturesTabContent
            :content-id="2"
            :content-title="'Share your bookmarks'"
            :content-description="'Easly share your bookmarks and collections with others. Create a sharable link that you can send at the click of a button.'"
            :content-image="'illustration-features-tab-3.svg'"
            :active-tab="activeTab"
        />
    </div>
</template>
<script>
import SectionFeaturesTabButton from './SectionFeaturesTabButton.vue';
import SectionFeaturesTabContent from './SectionFeaturesTabContent.vue';
export default {
    name: 'SectionFeaturesTab',
    components: {
        SectionFeaturesTabButton,
        SectionFeaturesTabContent
    },
    data() {
        return {
            activeTab: 0
        }
    },
    methods: {
        onFeaturesTabButtonClick(btnId){
            this.activeTab = btnId
        }
    }
}
</script>
<style scoped>
.buttonTabBox {
    @apply
        flex
        flex-col
        lg:flex-row
        px-6
        mb-16
        justify-center
}
</style>