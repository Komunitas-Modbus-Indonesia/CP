<template>
    <!-- About Section -->
    <PageSection variant="default"
                 :id="props.id">
        <!-- Title -->
        <PageSectionHeader title="*Tentang* Kami"
                           subtitle=""/>

        <!-- Content -->
        <PageSectionContent>
            <!-- About Template -->
            <ArticleInfoBlock image="images/logo/KMI.jpg"
                              :paragraphs="[
                                  `<b>Komunitas Modbus Indonesia (KMI)</b> didedikasikan untuk standardisasi, edukasi, dan implementasi protokol komunikasi Modbus di lingkungan industri tanah air. Kami menjembatani kesenjangan antara akademisi, engineer lapangan, dan vendor teknologi.`,
                                  `Di era Industri 4.0, protokol komunikasi yang handal menjadi fondasi penting dalam sistem otomasi industri. Modbus, sebagai salah satu protokol yang paling banyak digunakan, memerlukan pemahaman dan implementasi yang tepat untuk memaksimalkan efisiensi operasional.`,
                                  `Melalui forum diskusi, workshop, dan kolaborasi dengan berbagai pemangku kepentingan, KMI berkomitmen untuk meningkatkan kompetensi profesional di bidang komunikasi industri dan mendorong adopsi standar terbaik dalam implementasi Modbus di Indonesia.`
                              ]"/>
        </PageSectionContent>

        <!-- Footer -->
        <PageSectionFooter title="Bergabung Bersama *Kami*"
                           description="Ingin menjadi bagian dari Komunitas Modbus Indonesia? Bergabunglah dengan kami dan tingkatkan kompetensi di bidang komunikasi industri!"
                           :include-divider="true"
                           button-label="Join Us"
                           button-fa-icon="fa-solid fa-user-plus"
                           button-url="https://web.facebook.com/share/g/18GmXGAkYV/"/>
    </PageSection>
</template>

<script setup>
import PageSection from "/src/vue/components/layout/PageSection.vue"
import PageSectionHeader from "/src/vue/components/layout/PageSectionHeader.vue"
import PageSectionContent from "/src/vue/components/layout/PageSectionContent.vue"
import PageSectionFooter from "/src/vue/components/layout/PageSectionFooter.vue"
import ArticleInfoBlock from "/src/vue/components/articles/ArticleInfoBlock.vue"

const props = defineProps({
    id: String
})
</script>

<style lang="scss" scoped>
@import "/src/scss/_theming.scss";
</style>