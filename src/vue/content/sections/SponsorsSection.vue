<template>
    <section id="sponsor" class="sponsors-section">
        <!-- Fade edge overlays -->
        <div class="fade-left" aria-hidden="true"/>
        <div class="fade-right" aria-hidden="true"/>

        <!-- Header -->
        <!-- <div class="sponsors-header"> -->
            <!-- <h3 class="sponsors-title">Didukung Oleh <span class="sponsors-highlight">Mitra Strategis</span></h3> -->
            <!-- <p class="sponsors-subtitle">Bersama kami, mereka mempercayakan solusi terbaik</p> -->
        <!-- </div> -->

        <!-- Marquee -->
        <div class="marquee-viewport">
            <div class="marquee-track">
                <!-- Original list -->
                <div
                    v-for="(sponsor, i) in sponsors"
                    :key="`a-${i}`"
                    class="marquee-item"
                >
                    <img
                        :src="sponsor.logo"
                        :alt="sponsor.name"
                        class="sponsor-logo"
                        @error="onImgError($event)"
                    />
                    <span class="sponsor-label">{{ sponsor.name }}</span>
                </div>

                <!-- Duplicated list — seamless loop -->
                <div
                    v-for="(sponsor, i) in sponsors"
                    :key="`b-${i}`"
                    class="marquee-item"
                    aria-hidden="true"
                >
                    <img
                        :src="sponsor.logo"
                        :alt="sponsor.name"
                        class="sponsor-logo"
                        @error="onImgError($event)"
                    />
                    <span class="sponsor-label">{{ sponsor.name }}</span>
                </div>
            </div>
        </div>
    </section>
</template>

<script setup>
import { ref } from 'vue'

// import.meta.env.BASE_URL resolves to '/' in dev and the configured
// base ('/vue-agency-landing-page-template/') in production, so image
// paths are always correct regardless of environment.
const base = import.meta.env.BASE_URL
const img = (file) => `${base}images/sponsor/${file}`

const sponsors = ref([
   { name: '',                         logo: img('sponsor1.png') },
    { name: '',                     logo: img('sponsor2.png') },
    { name: '',                logo: img('sponsor3.png') },
    { name: '',                    logo: img('sponsor4.png') },
    { name: '',                          logo: img('sponsor5.png') },
    { name: '',                 logo: img('sponsor6.png') },
    { name: '',                   logo: img('sponsor7.png') },
    { name: '',                      logo: img('sponsor8.png') },
    { name: '',    logo: img('sponsor9.png') },
    { name: '',                           logo: img('sponsor10.png') },
    { name: '',                    logo: img('sponsor11.png') },
    { name: '',                     logo: img('sponsor12.png') },
])

/**
 * When a logo image fails to load, hide the <img> so the
 * text label becomes the only visible element inside the card.
 */
const onImgError = (event) => {
    event.target.style.display = 'none'
}
</script>

<style lang="scss" scoped>
@import "/src/scss/_variables.scss";
@import "/src/scss/_theming.scss";

/* ─────────────────────────────────────────
   Section wrapper
───────────────────────────────────────── */
.sponsors-section {
    position: relative;
    background-color: #ffffff;
    padding: 1.5rem 0 2.5rem;
    overflow: hidden;
    border-bottom: 1px solid rgba(0, 0, 0, 0.06);
}

/* ─────────────────────────────────────────
   Fade-edge overlays
───────────────────────────────────────── */
.fade-left,
.fade-right {
    position: absolute;
    top: 0;
    width: 140px;
    height: 100%;
    z-index: 3;
    pointer-events: none;
}

.fade-left {
    left: 0;
    background: linear-gradient(to right, #ffffff 0%, transparent 100%);
}

.fade-right {
    right: 0;
    background: linear-gradient(to left, #ffffff 0%, transparent 100%);
}

/* ─────────────────────────────────────────
   Header
───────────────────────────────────────── */
.sponsors-header {
    text-align: center;
    padding: 0 1.25rem;
    margin-bottom: 2.25rem;
    position: relative;
    z-index: 2;
}

.sponsors-title {
    color: #1A2238;
    font-size: clamp(1.2rem, 3vw, 1.65rem);
    font-weight: 700;
    margin: 0 0 0.4rem;
    letter-spacing: 0.2px;
}

.sponsors-highlight {
    color: $primary;
}

.sponsors-subtitle {
    color: rgba(#1A2238, 0.45);
    font-size: 0.875rem;
    margin: 0;
}

/* ─────────────────────────────────────────
   Marquee viewport
───────────────────────────────────────── */
.marquee-viewport {
    overflow: hidden;
    white-space: nowrap;
    width: 100%;
}

/* ─────────────────────────────────────────
   Marquee track
   Width intentionally wider than viewport;
   animation shifts by -50% → seamless loop
───────────────────────────────────────── */
.marquee-track {
    display: inline-flex;
    align-items: center;
    gap: 1.5rem;
    padding: 0.5rem 0;
    animation: marquee-scroll 30s linear infinite;
    will-change: transform;

    &:hover {
        animation-play-state: paused;
    }
}

/* ─────────────────────────────────────────
   Individual sponsor card
───────────────────────────────────────── */
.marquee-item {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    flex-shrink: 0;
    padding: 0 30px;
    background: transparent;
    border: none;
    box-shadow: none;
    cursor: default;

    &:hover {
        .sponsor-logo {
            transform: scale(1.08);
            opacity: 0.85;
        }
    }
}

/* ─────────────────────────────────────────
   Logo image — white/grey in idle state
───────────────────────────────────────── */
.sponsor-logo {
    display: block;
    height: 42px;
    max-width: 130px;
    object-fit: contain;
    transition: transform 0.3s ease;

    @media (min-width: 768px) {
        height: 52px;
    }
}

/* ─────────────────────────────────────────
   Text label — shown when no logo is set
   or as caption below logo
───────────────────────────────────────── */
.sponsor-label {
    display: none;
}

/* ─────────────────────────────────────────
   Keyframes
───────────────────────────────────────── */
@keyframes marquee-scroll {
    from { transform: translateX(0); }
    to   { transform: translateX(-50%); }
}

/* ─────────────────────────────────────────
   Accessibility — respect reduced-motion
───────────────────────────────────────── */
@media (prefers-reduced-motion: reduce) {
    .marquee-track {
        animation: none;
        flex-wrap: wrap;
        justify-content: center;
    }
}
</style>
