<template>
    <section id="learn" class="learn-section">
        <div class="container-xxl">

        <!-- Header -->
        <div class="learn-header">
            <!-- <p class="learn-eyebrow">Webinar &amp; Tutorial</p> -->
            <h2 class="learn-title">Knowledge/<span class="learn-highlight">Pengetahuan</span></h2>
            <p class="learn-subtitle">
                Kumpulan rekaman webinar, tutorial, dan sesi edukasi Komunitas Modbus Indonesia.
            </p>
        </div>

        <!-- Video Grid -->
        <div class="learn-grid">
            <a
                v-for="(video, i) in webinars"
                :key="i"
                :href="video.url"
                target="_blank"
                rel="noopener noreferrer"
                class="video-card"
                :title="video.title"
            >
                <!-- Thumbnail -->
                <div class="video-thumb-wrapper">
                    <img
                        :src="video.thumbnail"
                        :alt="video.title"
                        class="video-thumb"
                        loading="lazy"
                    />
                    <!-- Overlay + Play icon -->
                    <div class="video-overlay">
                        <div class="play-btn">
                            <i class="fa-solid fa-play play-icon"/>
                        </div>
                    </div>
                    <!-- Badge -->
                    <span class="video-badge">{{ video.tag }}</span>
                </div>

                <!-- Title -->
                <div class="video-body">
                    <h3 class="video-title">{{ video.title }}</h3>
                </div>
            </a>
        </div>

        <!-- CTA -->
        <div class="learn-cta-wrapper">
            <a
                href="https://www.youtube.com/@KomunitasModbusIndonesia"
                target="_blank"
                rel="noopener noreferrer"
                class="btn-youtube"
            >
                <i class="fa-brands fa-youtube btn-yt-icon"/>
                Lihat Semua Video di YouTube KMI
            </a>
        </div>

        </div>
    </section>
</template>

<script setup>
import { ref } from 'vue'

// YouTube thumbnail helper — returns maxresdefault thumbnail from a video ID
const yt = (id) => `https://i.ytimg.com/vi/${id}/mqdefault.jpg`
const ytUrl = (id) => `https://www.youtube.com/watch?v=${id}`

const webinars = ref([
    {
        title:     'PRA SILANAS APA BISA NODE RED SEBAGAI DASHBOARD BMS',
        tag:       'Modbus',
        url:       ytUrl('d4-PCa4HU4s'),
        thumbnail: yt('d4-PCa4HU4s'),
    },
    {
        title:     'Workshop Canbus',
        tag:       'CANBUS',
        url:       ytUrl('QBvDxWUyChU'),
        thumbnail: yt('QBvDxWUyChU'),
    },
    {
        title:     'PRA WORKSHOP KMI 2025 - PELATIHAN DASAR AI UNTUK ENGINEER',
        tag:       'AI',
        url:       ytUrl('Pact3LHqESc'),
        thumbnail: yt('Pact3LHqESc'),
    },
    {
        title:     'PRA SILANAS #6 Implementasi Industrial Modbus LoraWAN',
        tag:       'LoraWAN',
        url:       ytUrl('FSvJxYtZfJ0'),
        thumbnail: yt('FSvJxYtZfJ0'),
    },
    {
        title:     'PRA SILANAS 6 IMPLEMENTASI PZEM UNTUK PENGUKURAN LISTRIK 3 PHASE',
        tag:       '',
        url:       ytUrl('ZeyqJuyW8WE'),
        thumbnail: yt('ZeyqJuyW8WE'),
    },
    {
        title:     'Pra Silanas 5 ke 6 integrasi protokol MQTT & rest API pada node red dan Flutter',
        tag:       'MQTT',
        url:       ytUrl('cahW2ktHEuk'),
        thumbnail: yt('cahW2ktHEuk'),
    },
    {
        title:     'Pra silanas 5 ke 3 - Belajar SCADA dengan software SmartICS',
        tag:       'SmartICS',
        url:       ytUrl('Q8b4tKYRsFI'),
        thumbnail: yt('Q8b4tKYRsFI'),
    },
    {
        title:     'Pra Silanas 5 Ke 5 implementasi monitoring energy',
        tag:       '',
        url:       ytUrl('mLlv-LXIV4k'),
        thumbnail: yt('mLlv-LXIV4k'),
    },
])
</script>

<style lang="scss" scoped>
@import "/src/scss/_variables.scss";
@import "/src/scss/_theming.scss";

/* ─────────────────────────────────────────
   Section
───────────────────────────────────────── */
.learn-section {
    background-color: #ffffff;
    padding: 5rem 0;
}

/* ─────────────────────────────────────────
   Header
───────────────────────────────────────── */
.learn-header {
    text-align: center;
    max-width: 640px;
    margin: 0 auto 3.5rem;
}

.learn-eyebrow {
    font-size: 0.78rem;
    font-weight: 700;
    letter-spacing: 2px;
    text-transform: uppercase;
    color: #FF0000;
    margin: 0 0 0.6rem;
}

.learn-title {
    font-size: clamp(1.6rem, 4vw, 2.4rem);
    font-weight: 800;
    color: #1A2238;
    margin: 0 0 0.9rem;
    letter-spacing: 1px;
}

.learn-highlight {
    color: $primary;
}

.learn-subtitle {
    font-size: 0.95rem;
    color: rgba(#1A2238, 0.55);
    line-height: 1.7;
    margin: 0;
}

/* ─────────────────────────────────────────
   Grid — 4 col desktop, 2 col tablet, 2 col mobile
───────────────────────────────────────── */
.learn-grid {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 1.25rem;

    @media (max-width: 1100px) {
        grid-template-columns: repeat(3, 1fr);
    }

    @media (max-width: 767px) {
        grid-template-columns: repeat(2, 1fr);
    }

    @media (max-width: 400px) {
        grid-template-columns: 1fr;
    }
}

/* ─────────────────────────────────────────
   Card — entire card is an <a> link
───────────────────────────────────────── */
.video-card {
    display: flex;
    flex-direction: column;
    border-radius: 12px;
    overflow: hidden;
    background: #ffffff;
    box-shadow: 0 2px 12px rgba(0, 0, 0, 0.07);
    text-decoration: none;
    color: inherit;
    transition: transform 0.3s ease, box-shadow 0.3s ease;

    &:hover {
        transform: translateY(-5px);
        box-shadow: 0 10px 28px rgba(0, 0, 0, 0.13);
        text-decoration: none;
        color: inherit;

        .video-thumb {
            transform: scale(1.06);
        }

        .video-overlay {
            opacity: 1;
        }

        .play-btn {
            transform: translate(-50%, -50%) scale(1.12);
        }
    }
}

/* ─────────────────────────────────────────
   Thumbnail container
───────────────────────────────────────── */
.video-thumb-wrapper {
    position: relative;
    width: 100%;
    aspect-ratio: 16 / 9;
    overflow: hidden;
    background: #0f0f0f;
}

.video-thumb {
    width: 100%;
    height: 100%;
    object-fit: cover;
    display: block;
    transition: transform 0.4s ease;
}

/* ─────────────────────────────────────────
   Overlay
───────────────────────────────────────── */
.video-overlay {
    position: absolute;
    inset: 0;
    background: linear-gradient(
        to top,
        rgba(0, 0, 0, 0.55) 0%,
        rgba(0, 0, 0, 0.15) 50%,
        transparent 100%
    );
    opacity: 0.7;
    transition: opacity 0.3s ease;
}

/* ─────────────────────────────────────────
   Play button
───────────────────────────────────────── */
.play-btn {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    width: 42px;
    height: 42px;
    border-radius: 50%;
    background: rgba(255, 255, 255, 0.92);
    display: flex;
    align-items: center;
    justify-content: center;
    transition: transform 0.3s ease, background 0.2s ease;
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.3);

    .video-card:hover & {
        background: #FF0000;
    }
}

.play-icon {
    font-size: 0.75rem;
    color: #1A2238;
    margin-left: 2px; // optical center for play triangle

    .video-card:hover & {
        color: #ffffff;
    }
}

/* ─────────────────────────────────────────
   Category badge
───────────────────────────────────────── */
.video-badge {
    position: absolute;
    bottom: 8px;
    left: 8px;
    font-size: 0.62rem;
    font-weight: 700;
    letter-spacing: 1px;
    text-transform: uppercase;
    color: #ffffff;
    background: rgba($primary, 0.85);
    border-radius: 4px;
    padding: 0.15rem 0.5rem;
    backdrop-filter: blur(4px);
}

/* ─────────────────────────────────────────
   Card body — title with 2-line clamp
───────────────────────────────────────── */
.video-body {
    padding: 0.85rem 0.9rem 1rem;
    flex: 1;
}

.video-title {
    font-size: 0.82rem;
    font-weight: 700;
    color: #1A2238;
    line-height: 1.4;
    margin: 0;
    // 2-line clamp
    display: -webkit-box;
    -webkit-line-clamp: 2;
    -webkit-box-orient: vertical;
    overflow: hidden;
}

/* ─────────────────────────────────────────
   CTA button
───────────────────────────────────────── */
.learn-cta-wrapper {
    display: flex;
    justify-content: center;
    margin-top: 3rem;
}

.btn-youtube {
    display: inline-flex;
    align-items: center;
    gap: 0.55rem;
    padding: 0.75rem 2rem;
    border: 2px solid #FF0000;
    border-radius: 10px;
    color: #FF0000;
    background: transparent;
    font-size: 0.9rem;
    font-weight: 700;
    letter-spacing: 0.3px;
    text-decoration: none;
    transition: background-color 0.25s ease, color 0.25s ease, transform 0.2s ease;

    &:hover {
        background-color: #FF0000;
        color: #ffffff;
        transform: scale(1.03);
        text-decoration: none;
    }
}

.btn-yt-icon {
    font-size: 1.25rem;
}
</style>
