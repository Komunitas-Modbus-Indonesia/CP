<template>
    <!-- Navigation -->
    <Navigation logo="images/logo/KMImain.png"
                label=""/>

    <!-- Content Display -->
    <router-view/>

    <!-- Footer -->
    <footer class="kmi-footer">
        <div class="container-xxl">

            <!-- Top grid -->
            <div class="row kmi-footer-top">

                <!-- Col 1: Brand -->
                <div class="col-12 col-lg-4 kmi-footer-col">
                    <img src="/images/logo/KMImain.png" alt="KMI Logo" class="kmi-footer-logo"/>
                    <p class="kmi-footer-desc">
                        Wadah independen bagi para engineer, teknisi, dan praktisi industri
                        untuk berkolaborasi dan berbagi pengetahuan seputar protokol Modbus
                        dan Industrial IoT di Indonesia.
                    </p>
                    <!-- Social icons -->
                    <!-- <div class="kmi-socials">
                        <a href="https://web.facebook.com/share/g/18GmXGAkYV/" target="_blank" rel="noopener" class="kmi-social-btn" title="Facebook">
                            <i class="fa-brands fa-facebook-f"/>
                        </a>
                        <a href="https://www.youtube.com/@KomunitasModbusIndonesia" target="_blank" rel="noopener" class="kmi-social-btn" title="YouTube">
                            <i class="fa-brands fa-youtube"/>
                        </a>
                        <a href="https://wa.me/6281555305255" target="_blank" rel="noopener" class="kmi-social-btn" title="WhatsApp">
                            <i class="fa-brands fa-whatsapp"/>
                        </a>
                    </div>
                    < Legal micro-links -->
                    <!--<div class="kmi-legal-links">
                        <a href="/privacy-policy" class="kmi-legal-link">Kebijakan Privasi</a>
                        <span class="kmi-legal-sep">·</span>
                        <a href="/license" class="kmi-legal-link">Lisensi</a>
                    </div> -->
                </div>

                <!-- Col 2: Nav links -->
                <div class="col-12 col-sm-6 col-lg-4 kmi-footer-col">
                    <p class="kmi-footer-heading">TAUTAN POPULER</p>
                    <nav class="d-flex flex-column kmi-nav-links">
                        <a href="#about"   class="kmi-nav-link"><i class="fa-solid fa-arrow-right kmi-link-arrow"/>Tentang KMI</a>
                        <a href="#produk"  class="kmi-nav-link"><i class="fa-solid fa-arrow-right kmi-link-arrow"/>Produk</a>
                        <a href="#learn"   class="kmi-nav-link"><i class="fa-solid fa-arrow-right kmi-link-arrow"/>Belajar</a>
                        <a href="#event"   class="kmi-nav-link"><i class="fa-solid fa-arrow-right kmi-link-arrow"/>Event</a>
                        <a href="#faq"     class="kmi-nav-link"><i class="fa-solid fa-arrow-right kmi-link-arrow"/>FAQ</a>
                        <a href="#contact" class="kmi-nav-link"><i class="fa-solid fa-arrow-right kmi-link-arrow"/>Kontak</a>
                    </nav>
                </div>

                <!-- Col 3: Contact -->
                <div class="col-12 col-sm-6 col-lg-4 kmi-footer-col">
                    <p class="kmi-footer-heading">HUBUNGI KAMI</p>
                    <p class="kmi-footer-desc">Punya pertanyaan atau ingin bergabung? Hubungi kami melalui salah satu channel di bawah ini.</p>
                    <ul class="kmi-contact-list">
                        <li>
                            <i class="fa-brands fa-whatsapp kmi-contact-icon"/>
                            <a href="https://wa.me/6281555305255" target="_blank" rel="noopener">+62815 5530 5255</a>
                        </li>
                        <li>
                            <i class="fa-brands fa-youtube kmi-contact-icon"/>
                            <a href="https://www.youtube.com/@KomunitasModbusIndonesia" target="_blank" rel="noopener">YouTube KMI</a>
                        </li>
                        <li>
                            <i class="fa-brands fa-facebook kmi-contact-icon"/>
                            <a href="https://web.facebook.com/share/g/18GmXGAkYV/" target="_blank" rel="noopener">Facebook Group KMI</a>
                        </li>
                    </ul>
                </div>

            </div><!-- /row -->

            <!-- Bottom bar -->
            <div class="kmi-footer-bottom">
                <p class="kmi-copyright">
                    Copyright &copy; 2026 Komunitas Modbus Indonesia. All rights reserved.
                </p>
            </div>

        </div>
    </footer>
</template>

<script setup>
import Navigation from "/src/vue/components/nav/Navigation.vue"
</script>

<style lang="scss" scoped>
@import "/src/scss/_theming.scss";

/* ─────────────────────────────────────────
   Footer shell
───────────────────────────────────────── */
.kmi-footer {
    background-color: #0d1526;
    color: #cbd5e1;
    padding: 0 0 0;
    overflow: hidden;
}

/* ─────────────────────────────────────────
   Top grid row
───────────────────────────────────────── */
.kmi-footer-top {
    row-gap: 0;
    align-items: stretch;
}

.kmi-footer-col {
    text-align: left;
    padding: 2rem 1.5rem;

    &:not(:first-child) {
        padding: 2rem 1.5rem;

        @include media-breakpoint-up(lg) {
            padding: 3.5rem 2.5rem;
        }
    }
}

/* ─────────────────────────────────────────
   Brand column — accent panel
───────────────────────────────────────── */
.kmi-footer-col:first-child {
    background-color: #00AEEF;
    padding: 2rem 1.5rem;
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
    justify-content: center;

    @include media-breakpoint-up(lg) {
        padding: 3.5rem 2.5rem;
    }
}

.kmi-footer-logo {
    width: 160px;
    height: auto;
    object-fit: contain;
    margin-bottom: 1rem;

    @include media-breakpoint-up(lg) {
        width: 200px;
        margin-bottom: 1.5rem;
    }
}

.kmi-footer-desc {
    font-size: 0.875rem;
    color: rgba(255, 255, 255, 0.85);
    line-height: 1.8;
    margin: 0 0 1rem;
    max-width: 300px;

    @include media-breakpoint-up(lg) {
        margin: 0 0 1.75rem;
    }
}

/* ─────────────────────────────────────────
   Social icons (on accent panel)
───────────────────────────────────────── */
.kmi-socials {
    display: flex;
    gap: 0.6rem;
    margin-bottom: 1.5rem;
    justify-content: center;
}

.kmi-social-btn {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    width: 38px;
    height: 38px;
    border-radius: 6px;
    background: rgba(255, 255, 255, 0.2);
    color: #ffffff;
    font-size: 0.9rem;
    text-decoration: none;
    transition: background 0.2s ease;

    &:hover {
        background: rgba(255, 255, 255, 0.35);
    }
}

/* ─────────────────────────────────────────
   Legal micro-links (on accent panel)
───────────────────────────────────────── */
.kmi-legal-links {
    display: flex;
    align-items: center;
    gap: 0.5rem;
    justify-content: center;
}

.kmi-legal-link {
    font-size: 0.75rem;
    color: rgba(255, 255, 255, 0.65);
    text-decoration: none;
    transition: color 0.2s ease;

    &:hover {
        color: #ffffff;
    }
}

.kmi-legal-sep {
    color: rgba(255, 255, 255, 0.4);
    font-size: 0.75rem;
}

/* ─────────────────────────────────────────
   Column headings with accent underline
───────────────────────────────────────── */
.kmi-footer-heading {
    font-size: 1.05rem;
    font-weight: 700;
    letter-spacing: 0.5px;
    color: #ffffff;
    margin: 0 0 0.5rem;
    text-transform: none;
    position: relative;
    padding-bottom: 0.75rem;

    &::after {
        content: '';
        display: block;
        position: absolute;
        bottom: 0;
        left: 0;
        width: 40px;
        height: 3px;
        background-color: $primary;
        border-radius: 2px;
    }

    margin-bottom: 1.5rem;
}

/* ─────────────────────────────────────────
   Nav links (col 2)
───────────────────────────────────────── */
.kmi-nav-links {
    gap: 0.5rem;
}

.kmi-nav-link {
    font-size: 0.875rem;
    color: #94a3b8;
    text-decoration: none;
    transition: color 0.2s ease, padding-left 0.2s ease;
    width: fit-content;
    display: flex;
    align-items: center;
    gap: 0.5rem;

    &:hover {
        color: #ffffff;
        padding-left: 4px;
    }
}

.kmi-link-arrow {
    font-size: 0.7rem;
    color: $primary;
    flex-shrink: 0;
    transition: color 0.2s ease;
}

.kmi-nav-link:hover .kmi-link-arrow {
    color: #ffffff;
}

/* ─────────────────────────────────────────
   Contact list (col 3)
───────────────────────────────────────── */
.kmi-contact-list {
    list-style: none;
    padding: 0;
    margin: 0;
    display: flex;
    flex-direction: column;
    gap: 0.85rem;

    li {
        display: flex;
        align-items: center;
        gap: 0.75rem;
        font-size: 0.875rem;
    }

    a {
        color: #94a3b8;
        text-decoration: none;
        transition: color 0.2s ease;

        &:hover {
            color: #ffffff;
        }
    }
}

.kmi-contact-icon {
    font-size: 1rem;
    color: $primary;
    flex-shrink: 0;
    width: 16px;
    text-align: center;
}

/* ─────────────────────────────────────────
   Bottom bar
───────────────────────────────────────── */
.kmi-footer-bottom {
    border-top: 1px solid rgba(255, 255, 255, 0.07);
    padding: 1.25rem 0;
    text-align: center;
}

.kmi-copyright {
    font-size: 0.8rem;
    color: #64748b;
    margin: 0;
}
</style>