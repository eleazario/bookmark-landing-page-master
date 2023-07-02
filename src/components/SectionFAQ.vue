<template>
    <div class="sectionFAQ">
        <div class="questionBox">
            <SectionFAQItem
                :item-question="'What is Bookmark?'"
                :item-answer="'Qui ad elit nulla eiusmod laborum exercitation non cupidatat ea in. Ut id nulla fugiat labore ullamco exercitation amet consectetur mollit. Adipisicing sint veniam duis dolore consectetur ut id non non mollit eiusmod eiusmod. Cupidatat qui aute reprehenderit in eu pariatur quis culpa do fugiat reprehenderit ea. Anim dolore reprehenderit sit nisi dolore duis duis pariatur enim sunt eu deserunt officia ut.'"
            />
            <SectionFAQItem
                :item-question="'How can i request a new browser?'"
                :item-answer="'Qui ad elit nulla eiusmod laborum exercitation non cupidatat ea in. Ut id nulla fugiat labore ullamco exercitation amet consectetur mollit. Adipisicing sint veniam duis dolore consectetur ut id non non mollit eiusmod eiusmod. Cupidatat qui aute reprehenderit in eu pariatur quis culpa do fugiat reprehenderit ea. Anim dolore reprehenderit sit nisi dolore duis duis pariatur enim sunt eu deserunt officia ut.'"
            />
            <SectionFAQItem
                :item-question="'Is there a mobile app?'"
                :item-answer="'Qui ad elit nulla eiusmod laborum exercitation non cupidatat ea in. Ut id nulla fugiat labore ullamco exercitation amet consectetur mollit. Adipisicing sint veniam duis dolore consectetur ut id non non mollit eiusmod eiusmod. Cupidatat qui aute reprehenderit in eu pariatur quis culpa do fugiat reprehenderit ea. Anim dolore reprehenderit sit nisi dolore duis duis pariatur enim sunt eu deserunt officia ut.'"
            />
            <SectionFAQItem
                :item-question="'What about other Chromium browsers?'"
                :item-answer="'Qui ad elit nulla eiusmod laborum exercitation non cupidatat ea in. Ut id nulla fugiat labore ullamco exercitation amet consectetur mollit. Adipisicing sint veniam duis dolore consectetur ut id non non mollit eiusmod eiusmod. Cupidatat qui aute reprehenderit in eu pariatur quis culpa do fugiat reprehenderit ea. Anim dolore reprehenderit sit nisi dolore duis duis pariatur enim sunt eu deserunt officia ut.'"
            />
        </div>
        <div class="faqButtonBox">
            <BaseButton
                :btn-text="'More Info'"
                :btn-style="'primary'"
            />
        </div>
    </div>
</template>
<script>
import BaseButton from './BaseButton.vue';
import SectionFAQItem from './SectionFAQItem.vue';

export default {
    name: "SectionFAQ",
    components: { SectionFAQItem, BaseButton }
}
</script>
<style scoped>
.sectionFAQ {
    @apply
        px-8
        pt-4
        lg:w-[37.6rem]
        mx-auto
}

.questionBox {
    @apply
        mb-12
        lg:mb-14
}

.faqButtonBox {
    @apply
        w-28
        mx-auto
}
</style>