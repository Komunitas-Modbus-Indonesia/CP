<template>
    <!-- Event Highlight Section -->
    <PageSection variant="primary"
                 :id="props.id">
        <div class="event-section">
            <div class="row align-items-center g-4 g-lg-5">
                <!-- Event Poster Column - Order 1 on mobile, Order 2 on desktop -->
                <div class="col-12 col-lg-6 order-1 order-lg-2">
                    <div class="event-poster">
                        <img src="/images/event/silanas.jpeg" 
                             alt="SILANAS 7 Event Poster" 
                             class="img-fluid rounded-3 shadow-lg">
                    </div>
                </div>

                <!-- Text Content Column - Order 2 on mobile, Order 1 on desktop -->
                <div class="col-12 col-lg-6 order-2 order-lg-1">
                    <div class="event-content">
                        <!-- Badge -->
                        <div class="event-badge mb-3">
                            <span class="badge">
                                 EVENT TERDEKAT
                            </span>
                        </div>

                        <!-- Title -->
                        <h2 class="event-title mb-3">
                            SILANAS 7: Silaturahmi Nasional Praktisi Modbus & IoT
                        </h2>

                        <!-- Description -->
                        <p class="event-description mb-4">
                            Digitalisasi manajemen utilitas sektor Industri & bangunan gedung cerdas 
                            dalam mendukung target dekarbonisasi.
                        </p>

                        <!-- Event Details -->
                        <div class="event-details mb-4">
                            <div class="detail-item mb-3">
                                <i class="fa-regular fa-calendar detail-icon"></i>
                                <span class="detail-text">
                                    <strong>Tanggal:</strong> Sabtu, 4 April 2026 | 08.00 - 16.00 WIB
                                </span>
                            </div>
                            <div class="detail-item">
                                <i class="fa-solid fa-location-dot detail-icon"></i>
                                <span class="detail-text">
                                    <strong>Lokasi:</strong> Hotel Mercure Grand Mirama, Surabaya
                                </span>
                            </div>
                        </div>

                        <!-- CTA Button -->
                        <a href="https://bit.ly/REGSILANAS7" 
                           target="_blank" 
                           rel="noopener noreferrer"
                           class="btn btn-primary btn-lg">
                            <i class="fa-solid fa-user-plus me-2"></i>
                            Daftar Sekarang
                        </a>
                    </div>
                </div>
            </div>
        </div>
    </PageSection>
</template>

<script setup>
import PageSection from "/src/vue/components/layout/PageSection.vue"

const props = defineProps({
    id: String
})
</script>

<style lang="scss" scoped>
@import "/src/scss/_variables.scss";

.event-section {
    min-height: 500px;
    position: relative;
}

.event-content {
    @media (max-width: 991px) {
        text-align: center;
    }
}

.event-badge {
    .badge {
        background: linear-gradient(135deg, #dc2626 0%, #ef4444 100%);
        color: $white;
        padding: 0.5rem 1rem;
        font-size: 0.875rem;
        font-weight: 700;
        letter-spacing: 0.5px;
        border-radius: 50px;
        display: inline-block;
        box-shadow: 0 4px 12px rgba(220, 38, 38, 0.3);
    }
}

.event-title {
    font-family: $headings-font-family;
    color: $dark;
    font-size: clamp(1.75rem, 4vw, 2.5rem);
    line-height: 1.2;
    font-weight: 700;
}

.event-description {
    color: rgba($dark, 0.85);
    font-size: 1.125rem;
    line-height: 1.7;
}

.event-details {
    .detail-item {
        display: flex;
        align-items: flex-start;
        gap: 0.75rem;

        @media (max-width: 991px) {
            justify-content: center;
        }

        .detail-icon {
            color: $primary;
            font-size: 1.25rem;
            margin-top: 0.125rem;
            flex-shrink: 0;
        }

        .detail-text {
            color: rgba($dark, 0.8);
            font-size: 1rem;
            line-height: 1.6;

            strong {
                color: $dark;
                font-weight: 600;
            }
        }
    }
}

.btn-primary {
    background: linear-gradient(135deg, $primary 0%, #1d4ed8 100%);
    border: none;
    padding: 0.875rem 2rem;
    font-size: 1.125rem;
    font-weight: 600;
    border-radius: 50px;
    transition: all 0.3s ease;
    box-shadow: 0 4px 15px rgba($primary, 0.4);

    &:hover {
        transform: translateY(-2px);
        box-shadow: 0 6px 20px rgba($primary, 0.6);
        background: linear-gradient(135deg, #1d4ed8 0%, $primary 100%);
    }

    &:active {
        transform: translateY(0);
    }
}

.event-poster {
    position: relative;
    
    img {
        width: 100%;
        height: auto;
        border-radius: 1rem;
        box-shadow: 0 20px 40px rgba(0, 0, 0, 0.2);
        transition: transform 0.3s ease;

        &:hover {
            transform: scale(1.02);
        }
    }

    @media (max-width: 991px) {
        margin-top: 2rem;
        
        img {
            max-width: 500px;
            margin: 0 auto;
            display: block;
        }
    }
}
</style>
