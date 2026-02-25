<template>
    <section id="produk" class="products-section">
        <div class="container-xxl">
        <!-- Header -->
        <div class="products-header">
            <!-- <p class="products-eyebrow">Hardware Lokal Berkualitas</p> -->
            <h2 class="products-title">PRODUK <span class="products-highlight">KOMUNITAS</span></h2>
            <p class="products-subtitle">
                Dukung pengembangan komunitas dengan menggunakan produk hardware lokal berkualitas.
            </p>
        </div>

        <!-- Grid -->
        <div class="row g-4 products-grid">
            <div
                v-for="(product, i) in products"
                :key="i"
                class="col-lg-3 col-md-6 col-12"
            >
                <div class="product-card h-100 d-flex flex-column">
                    <!-- Image -->
                    <div class="product-image-wrapper">
                        <img
                            :src="product.image"
                            :alt="product.name"
                            class="product-image"
                        />
                    </div>

                    <!-- Body -->
                    <div class="product-body flex-grow-1">
                        <h3 class="product-name">{{ product.name }}</h3>
                        <p class="product-desc">{{ product.description }}</p>
                    </div>

                    <!-- Footer CTA -->
                    <div class="product-footer mt-auto">
                        <a
                            :href="product.waLink"
                            target="_blank"
                            rel="noopener noreferrer"
                            class="btn-wa"
                        >
                            <i class="fa-brands fa-whatsapp btn-wa-icon"/>
                            Pesan via WhatsApp
                        </a>
                    </div>
                </div>
            </div>
        </div>
        </div>
    </section>
</template>

<script setup>
import { ref } from 'vue'

const base = import.meta.env.BASE_URL
const img  = (file) => `${base}images/products/${file}`

// WhatsApp number — update to the community's WA number
const WA_NUMBER = '6281555305255'
const waLink = (productName) =>
    `https://wa.me/${WA_NUMBER}?text=${encodeURIComponent(`Halo, saya tertarik dengan produk: ${productName}`)}`

const products = ref([
    {
        name:        'SIMOR(Simple Modbus RTU)',
        description: 'Modul Gateway/Data Concentrator peralatan IED yang mempunyai protocol modbus rtu, Modbus TCP IP, lalu datanya diconvert menjadi protocol modbus TCP IP, Telegram, Iot Blynk, IEC60870-5-104 atau MQTT.',
        image:       img('product1.jpeg'),
        waLink:      waLink('SIMOR(Simple Modbus RTU)'),
    },
    {
        name:        'THM-30MD RS485 Module',
        description: 'Modul industrial konverter dan isolator komunikasi RS485 yang handal.',
        image:       img('product2.jpeg'),
        waLink:      waLink('THM-30MD RS485 Module'),
    },
    {
        name:        'Axial Labs SPD-T485-105',
        description: 'Surge Protective Device (Penangkal Petir) khusus untuk jalur komunikasi data RS485.',
        image:       img('product3.jpeg'),
        waLink:      waLink('Axial Labs SPD-T485-105'),
    },
    {
        name:        'Suriota Modbus Gateway IIoT',
        description: 'Perangkat Industrial IoT Gateway handal untuk mengintegrasikan data sensor Modbus RS-485 ke sistem cloud atau server lokal.',
        image:       img('product4.jpeg'),
        waLink:      waLink('Suriota Modbus Gateway IIoT'),
    }
])
</script>

<style lang="scss" scoped>
@import "/src/scss/_variables.scss";
@import "/src/scss/_theming.scss";

/* ─────────────────────────────────────────
   Section
───────────────────────────────────────── */
.products-section {
    background-color: #ffffff;
    padding: 5rem 0;
}

/* ─────────────────────────────────────────
   Header
───────────────────────────────────────── */
.products-header {
    text-align: center;
    max-width: 620px;
    margin: 0 auto 3.5rem;
}

.products-eyebrow {
    font-size: 0.78rem;
    font-weight: 700;
    letter-spacing: 2px;
    text-transform: uppercase;
    color: $primary;
    margin: 0 0 0.6rem;
}

.products-title {
    font-size: clamp(1.6rem, 4vw, 2.4rem);
    font-weight: 800;
    color: #1A2238;
    margin: 0 0 0.9rem;
    letter-spacing: 1px;
}

.products-highlight {
    color: $primary;
}

.products-subtitle {
    font-size: 0.95rem;
    color: rgba(#1A2238, 0.55);
    line-height: 1.7;
    margin: 0;
}

/* ─────────────────────────────────────────
   Grid
───────────────────────────────────────── */
.products-grid {
}

/* ─────────────────────────────────────────
   Card
───────────────────────────────────────── */
.product-card {
    display: flex;
    flex-direction: column;
    background: #ffffff;
    border-radius: 16px;
    box-shadow: 0 2px 16px rgba(0, 0, 0, 0.07);
    overflow: hidden;
    transition: transform 0.3s ease, box-shadow 0.3s ease;

    &:hover {
        transform: translateY(-6px);
        box-shadow: 0 12px 36px rgba(0, 0, 0, 0.11);
    }
}

/* ─────────────────────────────────────────
   Image
───────────────────────────────────────── */
.product-image-wrapper {
    width: 100%;
    overflow: hidden;
    background-color: #f1f5f9;
}

.product-image {
    width: 100%;
    height: 220px;
    object-fit: cover;
    object-position: center;
    display: block;
    transition: transform 0.4s ease;

    .product-card:hover & {
        transform: scale(1.04);
    }
}

/* ─────────────────────────────────────────
   Body
───────────────────────────────────────── */
.product-body {
    padding: 1.4rem 1.4rem 0.75rem;
    flex: 1;
}

.product-name {
    font-size: 1.05rem;
    font-weight: 700;
    color: #1A2238;
    margin: 0 0 0.5rem;
    line-height: 1.35;
}

.product-desc {
    font-size: 0.875rem;
    color: rgba(#1A2238, 0.6);
    line-height: 1.65;
    margin: 0;
}

/* ─────────────────────────────────────────
   Footer / CTA
───────────────────────────────────────── */
.product-footer {
    padding: 1rem 1.4rem 1.4rem;
}

.btn-wa {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    gap: 0.5rem;
    width: 100%;
    padding: 0.7rem 1.25rem;
    background-color: #25D366;
    color: #ffffff;
    font-size: 0.88rem;
    font-weight: 700;
    letter-spacing: 0.3px;
    border-radius: 10px;
    text-decoration: none;
    transition: background-color 0.25s ease, transform 0.2s ease;

    &:hover {
        background-color: #1ebe5a;
        transform: scale(1.02);
        color: #ffffff;
        text-decoration: none;
    }
}

.btn-wa-icon {
    font-size: 1.1rem;
}
</style>
