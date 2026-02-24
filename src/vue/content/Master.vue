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
                    <p class="kmi-footer-brand">KOMUNITAS MODBUS INDONESIA</p>
                    <p class="kmi-footer-desc">
                        Wadah independen bagi para engineer, teknisi, dan praktisi industri
                        untuk berkolaborasi dan berbagi pengetahuan seputar protokol Modbus
                        dan Industrial IoT di Indonesia.
                    </p>
                    <!-- Social icons -->
                    <div class="kmi-socials">
                        <a href="https://web.facebook.com/share/g/18GmXGAkYV/" target="_blank" rel="noopener" class="kmi-social-btn" title="Facebook">
                            <i class="fa-brands fa-facebook-f"/>
                        </a>
                        <a href="https://www.youtube.com/@KomunitasModbusIndonesia" target="_blank" rel="noopener" class="kmi-social-btn" title="YouTube">
                            <i class="fa-brands fa-youtube"/>
                        </a>
                        <a href="https://wa.me/6283140177186" target="_blank" rel="noopener" class="kmi-social-btn" title="WhatsApp">
                            <i class="fa-brands fa-whatsapp"/>
                        </a>
                    </div>
                    <!-- Legal micro-links -->
                    <div class="kmi-legal-links">
                        <a href="/privacy-policy" class="kmi-legal-link">Kebijakan Privasi</a>
                        <span class="kmi-legal-sep">·</span>
                        <a href="/license" class="kmi-legal-link">Lisensi</a>
                    </div>
                </div>

                <!-- Col 2: Nav links -->
                <div class="col-12 col-sm-6 col-lg-4 kmi-footer-col">
                    <p class="kmi-footer-heading">TAUTAN POPULER</p>
                    <nav class="d-flex flex-column kmi-nav-links">
                        <a href="#about"   class="kmi-nav-link">Tentang KMI</a>
                        <a href="#produk"  class="kmi-nav-link">Produk</a>
                        <a href="#learn"   class="kmi-nav-link">Belajar</a>
                        <a href="#event"   class="kmi-nav-link">Event</a>
                        <a href="#faq"     class="kmi-nav-link">FAQ</a>
                        <a href="#contact" class="kmi-nav-link">Kontak</a>
                    </nav>
                </div>

                <!-- Col 3: Contact -->
                <div class="col-12 col-sm-6 col-lg-4 kmi-footer-col">
                    <p class="kmi-footer-heading">HUBUNGI KAMI</p>
                    <p class="kmi-footer-desc">Punya pertanyaan atau ingin bergabung? Hubungi kami melalui salah satu channel di bawah ini.</p>
                    <ul class="kmi-contact-list">
                        <li>
                            <i class="fa-brands fa-whatsapp kmi-contact-icon"/>
                            <a href="https://wa.me/6283140177186" target="_blank" rel="noopener">+62 831-4017-7186</a>
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
    padding: 4rem 0 0;
}

/* ─────────────────────────────────────────
   Top grid row
───────────────────────────────────────── */
.kmi-footer-top {
    padding-bottom: 3rem;
    row-gap: 2.5rem;
}

.kmi-footer-col {
    text-align: left;
}

/* ─────────────────────────────────────────
   Brand column
───────────────────────────────────────── */
.kmi-footer-brand {
    font-size: 0.9rem;
    font-weight: 800;
    letter-spacing: 1.5px;
    color: #ffffff;
    margin: 0 0 1rem;
}

.kmi-footer-desc {
    font-size: 0.85rem;
    color: #94a3b8;
    line-height: 1.75;
    margin: 0 0 1.5rem;
    max-width: 320px;
}

/* ─────────────────────────────────────────
   Social icons
───────────────────────────────────────── */
.kmi-socials {
    display: flex;
    gap: 0.6rem;
    margin-bottom: 1.25rem;
}

.kmi-social-btn {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    width: 36px;
    height: 36px;
    border-radius: 50%;
    background: rgba(255, 255, 255, 0.08);
    color: #cbd5e1;
    font-size: 0.85rem;
    text-decoration: none;
    transition: background 0.2s ease, color 0.2s ease;

    &:hover {
        background: $primary;
        color: #ffffff;
    }
}

/* ─────────────────────────────────────────
   Legal micro-links
───────────────────────────────────────── */
.kmi-legal-links {
    display: flex;
    align-items: center;
    gap: 0.5rem;
}

.kmi-legal-link {
    font-size: 0.75rem;
    color: #64748b;
    text-decoration: none;
    transition: color 0.2s ease;

    &:hover {
        color: #cbd5e1;
    }
}

.kmi-legal-sep {
    color: #334155;
    font-size: 0.75rem;
}

/* ─────────────────────────────────────────
   Column headings (col 2 & 3)
───────────────────────────────────────── */
.kmi-footer-heading {
    font-size: 0.75rem;
    font-weight: 800;
    letter-spacing: 2px;
    color: #ffffff;
    margin: 0 0 1.25rem;
    text-transform: uppercase;
}

/* ─────────────────────────────────────────
   Nav links (col 2)
───────────────────────────────────────── */
.kmi-nav-links {
    gap: 0.6rem;
}

.kmi-nav-link {
    font-size: 0.875rem;
    color: #94a3b8;
    text-decoration: none;
    transition: color 0.2s ease;
    width: fit-content;

    &:hover {
        color: #ffffff;
    }
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
    gap: 0.75rem;

    li {
        display: flex;
        align-items: center;
        gap: 0.65rem;
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
    font-size: 0.78rem;
    color: #475569;
    margin: 0;
}
</style>