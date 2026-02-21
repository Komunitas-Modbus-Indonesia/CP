<template>
    <!-- Services Section -->
    <PageSection variant="primary"
                 :id="props.id">
        <!-- Title -->
        <PageSectionHeader title="Inisiatif & *Program*"
                           subtitle="This section can be used to describe what you offer!"/>

        <!-- Content -->
        <PageSectionContent>
            <ArticleFeatures>
                <ItemFeature title="SILANAS & Konferensi"
                             fa-icon="fa-solid fa-users"
                             description="Pertemuan tingkat nasional dan pameran hardware tahunan yang mempertemukan pakar otomasi untuk membahas tren terbaru dalam SCADA, PLC, dan Industrial IoT."/>

                <ItemFeature title="Technical Workshops"
                             fa-icon="fa-solid fa-laptop-code"
                             description="Sesi hands-on intensif yang mencakup integrasi Modbus, troubleshooting jaringan pabrik, dan pemetaan arsitektur sistem kendali."/>

                <ItemFeature title="Open-Source R&D"
                             fa-icon="fa-solid fa-code-branch"
                             description="Kolaborasi riset untuk mengembangkan library, driver, dan tooling secara open-source guna mempercepat adopsi teknologi lokal."/>
            </ArticleFeatures>
        </PageSectionContent>
    </PageSection>
</template>

<script setup>
import PageSection from "/src/vue/components/layout/PageSection.vue"
import PageSectionHeader from "/src/vue/components/layout/PageSectionHeader.vue"
import PageSectionContent from "/src/vue/components/layout/PageSectionContent.vue"
import ArticleFeatures from "/src/vue/components/articles/ArticleFeatures.vue"
import ItemFeature from "/src/vue/components/articles/items/ItemFeature.vue"

const props = defineProps({
    id: String
})
</script>

<style lang="scss" scoped>
@import "/src/scss/_theming.scss";
</style>