<template>
    <div class="hero__links">
        <a href="javascript:void(0)">
            <GPlayBrand />
            <span>Disponible en<span class="bold">Google Play</span></span>
        </a>
        <a href="javascript:void(0)">
            <AppleBrand />
            <span>Descárgalo en la <span class="bold">App Store</span></span>
        </a>
    </div>
</template>

<script setup lang="ts">
import GPlayBrand from '@/assets/icons/GPlayBrand.vue';
import AppleBrand from '@/assets/icons/AppleBrand.vue';
</script>

<style scoped lang="scss">
.hero__links {
    display: flex;
    gap: 1.8rem;

    a {
        min-width: 170px;
        display: inline-flex;
        justify-content: center;
        align-items: center;
        gap: 0.3rem;
        padding: 0.4rem 0.6rem;
        border-radius: 10px;
        border: 4px solid $neutral-gray;
        color: $background-light;
        background-color: $primary-color;
        transition:
            background-color 0.3s ease,
            box-shadow 0.3s ease,
            transform 0.3s ease;

        &:hover {
            background-color: $secondary-color;
            box-shadow: 0 6px 8px rgba($primary-color, 0.5);
            transform: translateY(-2px);
        }

        span {
            display: inline-flex;
            flex-direction: column;
            font-size: 0.75rem;

            .bold {
                font-weight: 700;
                font-size: 0.875rem;
            }
        }
    }
}
</style>
