<template>
    <article class="foxy-gallery-grid">
        <div class="gallery-container">
            <div class="gallery-grid">
                <div v-for="(image, index) in props.galleryItems"
                     :key="index"
                     class="gallery-item">
                    <img :src="image"
                         :alt="`Kegiatan ${index + 1}`"
                         class="gallery-image"/>
                </div>
            </div>
        </div>
    </article>
</template>

<script setup>
import { onMounted } from 'vue'

const props = defineProps({
    galleryItems: {
        type: Array,
        default: () => []
    }
})

onMounted(() => {
    console.log('Gallery mounted with items:', props.galleryItems)
})
</script>

<style lang="scss" scoped>
@import "/src/scss/_theming.scss";

article.foxy-gallery-grid {
    width: 100%;
    padding: 2rem 0;
    margin: 0 auto;
}

div.gallery-container {
    width: 100%;
    max-width: 1400px;
    margin: 0 auto;
    padding: 0 1rem;
}

div.gallery-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
    gap: 1.5rem;
    width: 100%;

    @include media-breakpoint-down(lg) {
        grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
        gap: 1.25rem;
    }

    @include media-breakpoint-down(md) {
        grid-template-columns: repeat(2, 1fr);
        gap: 1rem;
    }

    @include media-breakpoint-down(sm) {
        grid-template-columns: repeat(2, 1fr);
        gap: 0.75rem;
    }
}

div.gallery-item {
    position: relative;
    width: 100%;
    padding-bottom: 75%; /* 4:3 aspect ratio */
    overflow: hidden;
    border-radius: 12px;
    box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1);
    transition: transform 0.3s ease, box-shadow 0.3s ease;
    cursor: pointer;
    background: #f0f0f0;

    &:hover {
        transform: translateY(-5px);
        box-shadow: 0 8px 30px rgba(0, 0, 0, 0.2);

        img.gallery-image {
            transform: scale(1.05);
        }
    }
}

img.gallery-image {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    object-fit: cover;
    object-position: center;
    transition: transform 0.3s ease;
}
</style>
