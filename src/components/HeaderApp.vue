<template>
    <header class="header">
        <div class="header__container">
            <a href="/">TaskPro</a>
        </div>
    </header>
</template>

<script setup lang="ts"></script>

<style scoped lang="scss">
.header {
    background-color: $primary-color;
    padding: 0.6rem 1rem;

    &__container {
        @include containerWidth;
        @include flexCenter;
    }

    a {
        font-size: 2rem;
        font-weight: 700;
        color: $background-light;
    }
}
</style>
