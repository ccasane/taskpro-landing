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
    &__container {
        max-width: 990px;
        margin: auto;
        display: flex;
        justify-content: center;
        padding: 0.6rem 1rem;
    }
    a {
        font-size: 2rem;
        font-weight: 700;
        color: $background-light;
    }
}
</style>
