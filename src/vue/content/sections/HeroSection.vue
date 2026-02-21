<template>
    <!-- Heading Section -->
    <PageHeader :id="props.id"
                title="Komunitas *Modbus* Indonesia"
                subtitle="Komunitas untuk para pengguna, pengembang, dan penggemar *Modbus* di Indonesia. Bergabunglah dengan kami untuk berbagi pengetahuan, pengalaman, dan sumber daya terkait *Modbus*."
                logo-url="images/logo/KMImain.png">
        <template #buttons>
            <div class="hero-buttons d-flex flex-column flex-sm-row justify-content-center gap-3">
                <!-- Primary CTA - Event SILANAS 7 -->
                <a href="#event" class="btn btn-primary btn-lg px-4 py-3">
                    <i class="fa-solid fa-fire me-2"></i>
                    INFO SILANAS 7
                </a>
                
                <!-- Secondary CTA - About -->
                <a href="#about" class="btn btn-outline-light btn-lg px-4 py-3">
                    <i class="fa-solid fa-circle-info me-2"></i>
                    Tentang Komunitas
                </a>
            </div>
        </template>
    </PageHeader>
</template>

<script setup>
import PageHeader from "/src/vue/components/layout/PageHeader.vue"

const props = defineProps({
    id: String
})
</script>

<style lang="scss" scoped>
@import "/src/scss/_theming.scss";
@import "/src/scss/_variables.scss";

.hero-buttons {
    .btn {
        font-weight: 600;
        font-size: 1.125rem;
        border-radius: 50px;
        transition: all 0.3s ease;
        text-decoration: none;
        min-width: 200px;
        
        @media (max-width: 575px) {
            width: 100%;
            max-width: 300px;
        }
        
        i {
            font-size: 1.1rem;
        }
    }
    
    .btn-primary {
        background: linear-gradient(135deg, $primary 0%, #1d4ed8 100%);
        border: none;
        box-shadow: 0 4px 15px rgba($primary, 0.4);
        
        &:hover {
            transform: translateY(-3px);
            box-shadow: 0 6px 20px rgba($primary, 0.6);
            background: linear-gradient(135deg, #1d4ed8 0%, $primary 100%);
        }
        
        &:active {
            transform: translateY(-1px);
        }
    }
    
    .btn-outline-light {
        border: 2px solid rgba($white, 0.8);
        color: $white;
        background: rgba($white, 0.05);
        backdrop-filter: blur(10px);
        
        &:hover {
            background: rgba($white, 0.15);
            border-color: $white;
            color: $white;
            transform: translateY(-3px);
            box-shadow: 0 4px 15px rgba($white, 0.3);
        }
        
        &:active {
            transform: translateY(-1px);
        }
    }
}
</style>