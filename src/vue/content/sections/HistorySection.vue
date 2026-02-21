<template>
    <!-- Services Section -->
    <PageSection variant="default"
                 :id="props.id">
        <!-- Title -->
        <PageSectionHeader title="Jejak *Kegiatan*"
                           subtitle="Perjalanan komunitas kami dalam memajukan teknologi otomasi industri"/>

        <!-- Content -->
        <PageSectionContent>
            <ArticleTimeline>
                <ItemTimelineEntry title="SILANAS & IoT Expo Pertama"
                                   dateStart="Oktober 2025"
                                   dateEnd=""
                                   image="images/history/history-1.png"
                                   description="Silaturahmi Nasional pertama yang dihadiri 200+ profesional otomasi dari seluruh Indonesia. Event ini menampilkan pameran hardware, sesi panel tentang implementasi Modbus RTU/TCP, dan networking session yang mempertemukan vendor, integrator, dan end-user industri."
                                   :inverted="true"/>

                <ItemTimelineEntry title="Workshop Keamanan Siber Industri"
                                   dateStart="Januari 2026"
                                   dateEnd=""
                                   image="images/history/history-2.png"
                                   description="Workshop hands-on yang membahas vulnerability assessment pada protokol Modbus, implementasi firewall industrial, dan best practices dalam mengamankan komunikasi SCADA. Peserta mendapat sertifikat kompetensi dari praktisi bersertifikasi internasional."
                                   :inverted="false"/>

                <ItemTimelineEntry title="Inisiasi Riset Open-Source"
                                   dateStart="Februari 2026"
                                   dateEnd="Sekarang"
                                   image="images/history/history-3.png"
                                   description="Peluncuran proyek kolaboratif untuk mengembangkan Modbus library berbasis Python dan diagnostic tools open-source. Tim riset beranggotakan akademisi, engineer lapangan, dan developer yang berkomitmen menyediakan tooling gratis untuk komunitas industri Indonesia."
                                   :inverted="true"/>
            </ArticleTimeline>
        </PageSectionContent>
    </PageSection>
</template>

<script setup>
import PageSection from "/src/vue/components/layout/PageSection.vue"
import PageSectionHeader from "/src/vue/components/layout/PageSectionHeader.vue"
import PageSectionContent from "/src/vue/components/layout/PageSectionContent.vue"
import ArticleTimeline from "/src/vue/components/articles/ArticleTimeline.vue"
import ItemTimelineEntry from "/src/vue/components/articles/items/ItemTimelineEntry.vue"

const props = defineProps({
    id: String
})
</script>

<style lang="scss" scoped>
@import "/src/scss/_theming.scss";
</style>