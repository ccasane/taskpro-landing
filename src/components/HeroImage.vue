<template>
    <picture class="hero__image">
        <img
            src="@/assets/images/phone-one.png"
            alt="Imagen Iphone 15 Pro Max"
        />
    </picture>
</template>

<script setup lang="ts"></script>

<style scoped lang="scss">
.hero__image {
    position: relative;
    max-width: 240px;
    width: 100%;
}

@media (max-width: 767px) {
    .hero__image {
        display: none;
    }
}
</style>
