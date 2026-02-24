<template>
    <PageWrapper id="foxy-home-page"
                 :no-padding="true"
                 :sections="sections"/>
</template>

<script setup>
import PageWrapper from "/src/vue/components/layout/PageWrapper.vue"
import SectionInfo from "/src/models/SectionInfo.js"
import AboutSection from "/src/vue/content/sections/AboutSection.vue"
import ContactSection from "/src/vue/content/sections/ContactSection.vue"
import EventSection from "/src/vue/content/sections/EventSection.vue"
import FaqSection from "/src/vue/content/sections/FaqSection.vue"
import FeaturedProjectSection from "/src/vue/content/sections/FeaturedProjectSection.vue"
import HeroSection from "/src/vue/content/sections/HeroSection.vue"
import HistorySection from "/src/vue/content/sections/HistorySection.vue"
import SponsorsSection from "/src/vue/content/sections/SponsorsSection.vue"
import ProductsSection from "/src/vue/content/sections/ProductsSection.vue"
import LearnSection from "/src/vue/content/sections/LearnSection.vue"
import ContactKMISection from "/src/vue/content/sections/ContactKMISection.vue"
import PortfolioSection from "/src/vue/content/sections/PortfolioSection.vue"
import ReviewsSection from "/src/vue/content/sections/ReviewsSection.vue"
import ServicesSection from "/src/vue/content/sections/ServicesSection.vue"
import TeamSection from "/src/vue/content/sections/TeamSection.vue"

const sections = [
    new SectionInfo('hero',         HeroSection,            null,           null),
    // new SectionInfo('sponsor',      SponsorsSection,        'Sponsor',      'fa-solid fa-handshake'),
    new SectionInfo('about',        AboutSection,           'Tentang',      'pi pi-box'),
    new SectionInfo('produk',       ProductsSection,        'Produk',       'fa-solid fa-microchip'),
    new SectionInfo('learn',        LearnSection,           'Belajar',      'fa-brands fa-youtube'),
    // new SectionInfo('services',     ServicesSection,        'Services',     'pi pi-wrench'),
    new SectionInfo('event',        EventSection,           'Event',        'fa-solid fa-calendar-days'),
    // new SectionInfo('history',      HistorySection,         'History',      'pi pi-clock'),
    // new SectionInfo('featured',     FeaturedProjectSection, 'Zork',         'pi pi-qrcode'),
    new SectionInfo('portfolio',    PortfolioSection,       'Kegiatan',     'pi pi-folder-open'),
    // new SectionInfo('team',         TeamSection,            'Team',         'pi pi-users'),
    new SectionInfo('faq',          FaqSection,             'FAQ',          'pi pi-question-circle'),
    new SectionInfo('contact',      ContactKMISection,      'Kontak',       'fa-regular fa-envelope'),
    // new SectionInfo('reviews',      ReviewsSection,         'Reviews',      'fa-regular fa-comment'),
    // new SectionInfo('contact',      ContactSection,         'Contact',      'fa-regular fa-envelope')
]
</script>

<style lang="scss" scoped>
</style>