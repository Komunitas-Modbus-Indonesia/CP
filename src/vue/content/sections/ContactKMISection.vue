<template>
    <section id="contact" class="contact-section">
        <div class="container">
            <div class="contact-body">

                <!-- Header -->
                <p class="contact-eyebrow">INGIN BEKERJASAMA?</p>
                <h2 class="contact-title">
                    Kami Siap Berkolaborasi dalam Berbagai Inisiatif Industri
                </h2>
                <div class="contact-divider"/>

                <!-- Feature row -->
                <div class="contact-features">
                    <div class="contact-feature">
                        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none"
                             stroke="currentColor" stroke-width="2.2"
                             stroke-linecap="round" stroke-linejoin="round"
                             class="feature-icon">
                            <polyline points="9 10 4 15 9 20"/>
                            <path d="M20 4v7a4 4 0 0 1-4 4H4"/>
                        </svg>
                        <span class="feature-text">Merespon dengan cepat</span>
                    </div>
                    <div class="contact-feature">
                        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none"
                             stroke="currentColor" stroke-width="2.2"
                             stroke-linecap="round" stroke-linejoin="round"
                             class="feature-icon">
                            <path d="M22 16.92v3a2 2 0 0 1-2.18 2 19.79 19.79 0 0 1-8.63-3.07A19.5 19.5 0 0 1 4.69 12 19.79 19.79 0 0 1 1.62 3.38 2 2 0 0 1 3.6 1.21h3a2 2 0 0 1 2 1.72 12.84 12.84 0 0 0 .7 2.81 2 2 0 0 1-.45 2.11L7.91 8.8a16 16 0 0 0 6.29 6.29l.96-.96a2 2 0 0 1 2.1-.45 12.84 12.84 0 0 0 2.81.7A2 2 0 0 1 22 16.92z"/>
                        </svg>
                        <span class="feature-text">Dapat dihubungi kapan saja</span>
                    </div>
                </div>

                <!-- Description -->
                <p class="contact-desc">
                    Jika Anda atau perusahaan Anda membutuhkan dukungan teknis, kolaborasi acara,
                    sponsor, atau sekadar ingin berdiskusi seputar Modbus dan otomasi industri,
                    jangan ragu menghubungi tim pengurus kami. Kami akan memberikan respon terbaik
                    untuk Anda.
                </p>

                <!-- CTA boxes — two side by side -->
                <div class="contact-cta-row">

                    <!-- WhatsApp -->
                    <a
                        href="https://wa.me/6281555305255"
                        target="_blank"
                        rel="noopener noreferrer"
                        class="contact-cta"
                    >
                        <div class="cta-icon-box">
                            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none"
                                 stroke="currentColor" stroke-width="2.2"
                                 stroke-linecap="round" stroke-linejoin="round"
                                 class="cta-icon">
                                <path d="M22 16.92v3a2 2 0 0 1-2.18 2 19.79 19.79 0 0 1-8.63-3.07A19.5 19.5 0 0 1 4.69 12 19.79 19.79 0 0 1 1.62 3.38 2 2 0 0 1 3.6 1.21h3a2 2 0 0 1 2 1.72 12.84 12.84 0 0 0 .7 2.81 2 2 0 0 1-.45 2.11L7.91 8.8a16 16 0 0 0 6.29 6.29l.96-.96a2 2 0 0 1 2.1-.45 12.84 12.84 0 0 0 2.81.7A2 2 0 0 1 22 16.92z"/>
                            </svg>
                        </div>
                        <div class="cta-text">
                            <span class="cta-label">Hubungi kami via WhatsApp</span>
                            <span class="cta-number">+62 815-5530-5255</span>
                        </div>
                    </a>

                    <!-- WhatsApp 2 -->
                    <a
                        href="https://wa.me/6285250563939"
                        target="_blank"
                        rel="noopener noreferrer"
                        class="contact-cta"
                    >
                        <div class="cta-icon-box">
                            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none"
                                 stroke="currentColor" stroke-width="2.2"
                                 stroke-linecap="round" stroke-linejoin="round"
                                 class="cta-icon">
                                <path d="M22 16.92v3a2 2 0 0 1-2.18 2 19.79 19.79 0 0 1-8.63-3.07A19.5 19.5 0 0 1 4.69 12 19.79 19.79 0 0 1 1.62 3.38 2 2 0 0 1 3.6 1.21h3a2 2 0 0 1 2 1.72 12.84 12.84 0 0 0 .7 2.81 2 2 0 0 1-.45 2.11L7.91 8.8a16 16 0 0 0 6.29 6.29l.96-.96a2 2 0 0 1 2.1-.45 12.84 12.84 0 0 0 2.81.7A2 2 0 0 1 22 16.92z"/>
                            </svg>
                        </div>
                        <div class="cta-text">
                            <span class="cta-label">Hubungi kami via WhatsApp</span>
                            <span class="cta-number">+62 852-5056-3939</span>
                        </div>
                    </a>

                </div>

            </div>
        </div>
    </section>
    <SponsorsSection/>
</template>

<script setup>
import SponsorsSection from './SponsorsSection.vue';

// No reactive data needed — all content is static
</script>

<style lang="scss" scoped>
@import "/src/scss/_variables.scss";
@import "/src/scss/_theming.scss";

$accent: #4CB4E7;

/* ─────────────────────────────────────────
   Section
───────────────────────────────────────── */
.contact-section {
    background-color: #ffffff;
    padding: 5rem 0;
}

/* ─────────────────────────────────────────
   Single centered column
───────────────────────────────────────── */
.contact-body {
    max-width: 780px;
    display: flex;
    flex-direction: column;
    gap: 1.5rem;
}

/* ─────────────────────────────────────────
   Header
───────────────────────────────────────── */
.contact-eyebrow {
    font-size: 0.75rem;
    font-weight: 800;
    letter-spacing: 2.5px;
    text-transform: uppercase;
    color: $accent;
    margin: 0;
}

.contact-title {
    font-size: clamp(1.9rem, 4vw, 2.75rem);
    font-weight: 800;
    color: #1A2238;
    line-height: 1.2;
    margin: 0;
}

.contact-divider {
    width: 80px;
    height: 4px;
    background-color: $accent;
    border-radius: 2px;
}

/* ─────────────────────────────────────────
   Feature row — inline icons, no boxes
───────────────────────────────────────── */
.contact-features {
    display: flex;
    gap: 2.5rem;
    flex-wrap: wrap;
}

.contact-feature {
    display: flex;
    align-items: center;
    gap: 0.5rem;
}

.feature-icon {
    width: 18px;
    height: 18px;
    flex-shrink: 0;
    color: $accent;
}

.feature-text {
    font-size: 0.95rem;
    font-weight: 700;
    color: #1A2238;
}

/* ─────────────────────────────────────────
   Description
───────────────────────────────────────── */
.contact-desc {
    font-size: 0.975rem;
    color: #6c757d;
    line-height: 1.8;
    margin: 0;
}

/* ─────────────────────────────────────────
   CTA row — two boxes side by side
───────────────────────────────────────── */
.contact-cta-row {
    display: flex;
    gap: 2rem;
    flex-wrap: wrap;
}

.contact-cta {
    display: inline-flex;
    align-items: center;
    gap: 1rem;
    text-decoration: none;
    flex: 1;
    min-width: 220px;

    &:hover {
        text-decoration: none;

        .cta-icon-box {
            background-color: darken($primary, 8%);
        }

        .cta-icon-box--email {
            background-color: darken(#1A2238, 5%);
        }

        .cta-number {
            text-decoration: underline;
        }
    }
}

.cta-icon-box {
    flex-shrink: 0;
    width: 50px;
    height: 50px;
    border-radius: 6px;
    background-color: $primary;
    display: flex;
    align-items: center;
    justify-content: center;
    transition: background-color 0.25s ease;

    &--email {
        background-color: #1A2238;
    }
}

.cta-icon {
    width: 22px;
    height: 22px;
    color: #ffffff;
}

.cta-text {
    display: flex;
    flex-direction: column;
    gap: 0.15rem;
}

.cta-label {
    font-size: 0.8rem;
    color: #6c757d;
    font-weight: 500;
}

.cta-number {
    font-size: 1.6rem;
    font-weight: 800;
    color: $accent;
    line-height: 1;

    &--sm {
        font-size: 0.85rem;
        line-height: 1.4;
    }
}
</style>
