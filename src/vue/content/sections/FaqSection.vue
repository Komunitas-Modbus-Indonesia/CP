<template>
    <!-- FAQ Section -->
    <PageSection variant="default" :id="props.id">

        <!-- Title -->
        <PageSectionHeader title="TANYA *JAWAB*"
                           subtitle="Pertanyaan yang Sering Diajukan (FAQ)"/>

        <!-- Accordion -->
        <PageSectionContent>
            <div class="faq-accordion">
                <div
                    v-for="(item, index) in faqs"
                    :key="index"
                    class="faq-item"
                    :class="{ 'faq-item--open': activeIndex === index }"
                >
                    <!-- Header / trigger -->
                    <button class="faq-trigger" @click="toggle(index)" :aria-expanded="activeIndex === index">
                        <span class="faq-question">{{ item.question }}</span>
                        <span class="faq-chevron" :class="{ 'faq-chevron--open': activeIndex === index }">
                            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none"
                                 stroke="currentColor" stroke-width="2.5"
                                 stroke-linecap="round" stroke-linejoin="round">
                                <polyline points="6 9 12 15 18 9"/>
                            </svg>
                        </span>
                    </button>

                    <!-- Answer panel -->
                    <Transition name="faq-slide">
                        <div v-if="activeIndex === index" class="faq-body">
                            <p class="faq-answer" v-html="item.answer"/>
                        </div>
                    </Transition>
                </div>
            </div>
        </PageSectionContent>

    </PageSection>
</template>

<script setup>
import { ref } from 'vue'
import PageSection from "/src/vue/components/layout/PageSection.vue"
import PageSectionHeader from "/src/vue/components/layout/PageSectionHeader.vue"
import PageSectionContent from "/src/vue/components/layout/PageSectionContent.vue"

const props = defineProps({ id: String })

const activeIndex = ref(0)

const toggle = (index) => {
    activeIndex.value = activeIndex.value === index ? null : index
}

const faqs = [
    {
        question: 'Apa itu Komunitas Modbus Indonesia (KMI)?',
        answer:   'KMI adalah wadah independen bagi para engineer, teknisi, akademisi, dan praktisi industri untuk berkolaborasi, belajar, dan berbagi <b>praktik terbaik (best practices)</b> seputar implementasi protokol Modbus dan <b>Industrial IoT (IIoT)</b> di Indonesia.',
    },
    {
        question: 'Siapa saja yang bisa bergabung dengan komunitas ini?',
        answer:   'Keanggotaan terbuka untuk <b>semua kalangan!</b> Mulai dari mahasiswa/pelajar yang baru belajar mikrokontroler, engineer pabrik, system integrator, hingga vendor teknologi yang memiliki ketertarikan di bidang otomasi industri.',
    },
    {
        question: 'Apakah ada biaya untuk menjadi anggota KMI?',
        answer:   'Bergabung dengan grup diskusi utama kami (Telegram/WhatsApp) sepenuhnya <b>gratis</b>. Namun, untuk acara khusus seperti SILANAS, sertifikasi, atau technical workshop luring (offline), mungkin akan dikenakan biaya registrasi untuk keperluan operasional acara.',
    },
    {
        question: 'Bagaimana cara membagikan riset atau project open-source saya?',
        answer:   'Kami sangat mendukung semangat <b>open-source!</b> Anda bisa membagikan repository GitHub, topologi IoT, atau studi kasus integrasi SCADA langsung ke grup forum, atau menghubungi pengurus untuk mempresentasikannya pada sesi kopdar/workshop bulanan kami.',
    },
    {
        question: 'Apakah ada paket keanggotaan berbayar di KMI?',
        answer:   'Ya! KMI menyediakan <b>Premium Membership</b> bagi anggota yang ingin mendapatkan manfaat lebih. Dengan menjadi anggota premium, Anda akan mendapatkan akses ke <b>pelatihan eksklusif</b>, <b>source code</b> project industri siap pakai, serta <b>modul-modul Trainer Kit</b> yang dirancang khusus untuk mempercepat proses belajar implementasi Modbus dan IIoT. Hubungi pengurus kami untuk informasi lebih lanjut mengenai paket dan harganya.',
    },
]
</script>

<style lang="scss" scoped>
@import "/src/scss/_theming.scss";

/* ─────────────────────────────────────────
   Wrapper — centered single column
───────────────────────────────────────── */
.faq-accordion {
    width: 100%;
    display: flex;
    flex-direction: column;
    gap: 0;
}

/* ─────────────────────────────────────────
   Individual item
───────────────────────────────────────── */
.faq-item {
    border-bottom: 1px solid rgba(0, 0, 0, 0.08);

    &:first-child {
        border-top: 1px solid rgba(0, 0, 0, 0.08);
    }

    &--open {
        .faq-question {
            color: $primary;
        }
    }
}

/* ─────────────────────────────────────────
   Trigger button
───────────────────────────────────────── */
.faq-trigger {
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 1rem;
    padding: 1.15rem 0;
    background: transparent;
    border: none;
    cursor: pointer;
    text-align: left;

    &:focus-visible {
        outline: 2px solid $primary;
        outline-offset: 2px;
        border-radius: 4px;
    }
}

.faq-question {
    font-size: 1rem;
    font-weight: 700;
    color: #1A2238;
    line-height: 1.4;
    transition: color 0.2s ease;
}

/* ─────────────────────────────────────────
   Chevron icon
───────────────────────────────────────── */
.faq-chevron {
    flex-shrink: 0;
    width: 22px;
    height: 22px;
    color: $primary;
    transition: transform 0.3s ease;

    svg {
        width: 100%;
        height: 100%;
    }

    &--open {
        transform: rotate(180deg);
    }
}

/* ─────────────────────────────────────────
   Answer panel
───────────────────────────────────────── */
.faq-body {
    overflow: hidden;
}

.faq-answer {
    font-size: 0.95rem;
    color: #6c757d;
    line-height: 1.8;
    padding: 0 1.5rem 1.25rem 0;
    margin: 0;
}

/* ─────────────────────────────────────────
   Slide transition
───────────────────────────────────────── */
.faq-slide-enter-active,
.faq-slide-leave-active {
    transition: max-height 0.35s ease, opacity 0.3s ease;
    max-height: 600px;
    opacity: 1;
}

.faq-slide-enter-from,
.faq-slide-leave-to {
    max-height: 0;
    opacity: 0;
}
</style>