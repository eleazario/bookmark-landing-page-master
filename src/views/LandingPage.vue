<template>
    <main>
        <div class="titleBox">
            <div class="titleImageBox">
                <img src="../assets/images/illustration-hero.svg" alt="" class="titleImage">
                <div class="titleImageShapeBox">
                    <div class="titleImageShape"></div>
                </div>
            </div>
            <div class="titleTextBox">
                <h1>A Simple Bookmark Manager</h1>
                <p>A clean and simple interface to organize your favourite websites. Open a new browser tab and see your sites load instantly. Try it for free.</p>
                <div class="titleButtonBox">
                    <BaseButton 
                        :btn-style="'primary'"
                        :btn-text="'Get it on Chrome'"
                    />
                    <BaseButton 
                        :btn-style="'secondary'"
                        :btn-text="'Get it on Firefox'"
                    />
                </div>
            </div>
        </div>
        <section>
            <SectionTitleDescription 
                :section-title="'Features'"
                :section-description="'Our aim is to make it quick and easy for you to access your favourite websites. Your bookmarks sync between your devices so you can access them on the go.'"
            />
            <SectionFeaturesTab />
        </section>
        <section>
            <SectionTitleDescription 
                :section-title="'Download the extension'"
                :section-description="'We\'ve got more browsers in the pipeline. Please do let us know if you\'ve got a favourite you\'d like us to prioritize.'"
            />
            <SectionDownload />
        </section>
        <section>
            <SectionTitleDescription 
                :section-title="'Frequently Asked Questions'"
                :section-description="'Here are some of our FAQs. If you have any other questions you\'d like answered please feel free to email us.'"
            />
            <SectionFAQ />
        </section>
    </main>
</template>
<script>
import BaseButton from '@/components/BaseButton.vue';
import SectionDownload from '@/components/SectionDownload.vue';
import SectionFAQ from '@/components/SectionFAQ.vue';
import SectionFeaturesTab from '@/components/SectionFeaturesTab.vue';
import SectionTitleDescription from '@/components/SectionTitleDescription.vue';

export default {
    name: "LandingPage",
    components: {
        BaseButton,
        SectionTitleDescription,
        SectionFeaturesTab,
        SectionDownload,
        SectionFAQ
}
}
</script>
<style scoped>
main {
    @apply
        flex
        flex-col
        gap-[9.45rem]
        mb-32
        lg:mb-36
}

.titleBox {
    @apply
        grid
        grid-cols-1
        lg:grid-cols-2
}

.titleImageBox {
    @apply
        relative
        mb-14
        lg:mb-0
        lg:order-2
}

.titleImage {
    @apply
        sticky
        z-10
        px-2
}

.titleImageShapeBox {
    @apply
        absolute
        w-full
        h-full
        -bottom-2
        left-0
    }
    
.titleImageShape {
    @apply
        absolute
        bottom-0
        right-0
        bg-Soft-Blue
        h-4/5
        w-4/5
        rounded-l-full
}

.titleTextBox {
    @apply
        flex
        flex-col
        lg:justify-center
        lg:order-1
        text-center
        lg:text-start
        px-10
        lg:pl-[10.5rem]
}

.titleTextBox > h1 {
    @apply
        text-3xl
        lg:text-5xl
        text-gray-700
        font-medium
        mb-6
        lg:mb-7
}

.titleTextBox > p {
    @apply
        text-base
        lg:text-lg
        text-gray-400
}

.titleButtonBox {
    @apply
        flex
        mt-6
        lg:mt-8
        gap-3
        lg:gap-4
        lg:w-[21rem]
}
</style>