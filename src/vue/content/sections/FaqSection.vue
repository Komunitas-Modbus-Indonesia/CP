<template>
    <!-- FAQ Section -->
    <PageSection variant="default"
                 :id="props.id">
        <!-- Title -->
        <PageSectionHeader title="TANYA *JAWAB*"
                           subtitle="Pertanyaan yang Sering Diajukan (FAQ)"/>

        <!-- Content -->
        <PageSectionContent>
            <ArticleFaq>
                <ItemFaqQuestion question="Apa itu Komunitas Modbus Indonesia (KMI)?"
                                 answer="KMI adalah wadah independen bagi para engineer, teknisi, akademisi, dan praktisi industri untuk berkolaborasi, belajar, dan berbagi <b>praktik terbaik (best practices)</b> seputar implementasi protokol Modbus dan <b>Industrial IoT (IIoT)</b> di Indonesia."/>

                <ItemFaqQuestion question="Siapa saja yang bisa bergabung dengan komunitas ini?"
                                 answer="Keanggotaan terbuka untuk <b>semua kalangan!</b> Mulai dari mahasiswa/pelajar yang baru belajar mikrokontroler, engineer pabrik, system integrator, hingga vendor teknologi yang memiliki ketertarikan di bidang otomasi industri."/>

                <ItemFaqQuestion question="Apakah ada biaya untuk menjadi anggota KMI?"
                                 answer="Bergabung dengan grup diskusi utama kami (Telegram/WhatsApp) sepenuhnya <b>gratis</b>. Namun, untuk acara khusus seperti SILANAS, sertifikasi, atau technical workshop luring (offline), mungkin akan dikenakan biaya registrasi untuk keperluan operasional acara."/>

                <ItemFaqQuestion question="Bagaimana cara membagikan riset atau project open-source saya?"
                                 answer="Kami sangat mendukung semangat <b>open-source!</b> Anda bisa membagikan repository GitHub, topologi IoT, atau studi kasus integrasi SCADA langsung ke grup forum, atau menghubungi pengurus untuk mempresentasikannya pada sesi kopdar/workshop bulanan kami."/>
            </ArticleFaq>
        </PageSectionContent>

        <!-- Footer -->
        <PageSectionFooter title="Bergabung Bersama *Kami*"
                           description="Jadilah bagian dari komunitas yang terus belajar dan berkembang di bidang teknologi otomasi industri!"
                           :include-divider="true"
                           :description-text-class="`text-3`"
                           button-label="Gabung Sekarang"
                           button-fa-icon="fa-solid fa-user-plus"
                           button-url="https://web.facebook.com/share/g/18GmXGAkYV/"/>
    </PageSection>
</template>

<script setup>
import PageSection from "/src/vue/components/layout/PageSection.vue"
import PageSectionHeader from "/src/vue/components/layout/PageSectionHeader.vue"
import PageSectionContent from "/src/vue/components/layout/PageSectionContent.vue"
import PageSectionFooter from "/src/vue/components/layout/PageSectionFooter.vue"
import ArticleFaq from "/src/vue/components/articles/ArticleFaq.vue"
import ItemFaqQuestion from "/src/vue/components/articles/items/ItemFaqQuestion.vue"

const props = defineProps({
    id: String
})
</script>

<style lang="scss" scoped>
@import "/src/scss/_theming.scss";
</style>