<template>
    <!-- Gallery Section -->
    <PageSection variant="default"
                 :id="props.id">
        <!-- Title -->
        <PageSectionHeader title="Jejak *Kegiatan*"
                           subtitle="Dokumentasi kegiatan dan kolaborasi komunitas kami"/>

        <!-- Content -->
        <PageSectionContent>
            <ArticleGalleryCarousel :gallery-items="galleryItems"/>
        </PageSectionContent>
    </PageSection>
</template>

<script setup>
import PageSection from "/src/vue/components/layout/PageSection.vue"
import PageSectionHeader from "/src/vue/components/layout/PageSectionHeader.vue"
import PageSectionContent from "/src/vue/components/layout/PageSectionContent.vue"
import ArticleGalleryCarousel from "/src/vue/components/articles/ArticleGalleryCarousel.vue"

const props = defineProps({
    id: String
})

const galleryItems = [
    // "images/gallery/porto1.jpeg",
    // "images/gallery/porto2.jpeg",
    "images/gallery/porto3.jpeg",
    "images/gallery/porto4.jpeg",
    "images/gallery/porto5.jpeg",
    "images/gallery/porto6.jpeg",
    "images/gallery/porto7.jpeg",
    "images/gallery/porto8.jpeg",
    "images/gallery/porto9.jpeg",
    "images/gallery/porto10.jpeg"
]
</script>

<style lang="scss" scoped>
@import "/src/scss/_theming.scss";
</style>