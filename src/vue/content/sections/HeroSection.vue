<template>
    <!-- Heading Section -->
    <PageHeader :id="props.id"
                title="Komunitas *Modbus* Indonesia"
                subtitle="Komunitas untuk para pengguna, pengembang, dan penggemar *Modbus* di Indonesia. Bergabunglah dengan kami untuk berbagi pengetahuan, pengalaman, dan sumber daya terkait *Modbus*."
                logo-url="images/logo/logoutama.png"
                :show-button="true"
                button-icon="fa-solid fa-search"
                button-label="Find Out More"
                button-url="#about"/>
</template>

<script setup>
import PageHeader from "/src/vue/components/layout/PageHeader.vue"

const props = defineProps({
    id: String
})
</script>

<style lang="scss" scoped>
@import "/src/scss/_theming.scss";
</style>