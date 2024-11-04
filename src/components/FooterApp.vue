<template>
    <footer class="footer">
        <div class="footer__container">
            <p>
                © {{ dateFooter }} <a href="javascript:void(0)">TaskPro</a>.
                Todos los derechos reservados.
            </p>
            <div class="footer__links">
                <a href="javascript:void(0)" aria-label="Terms and Conditions"
                    >Términos y Condiciones</a
                >
                <a href="javascript:void(0)" aria-label="Privacy Policy"
                    >Política de Privacidad</a
                >
            </div>
        </div>
    </footer>
</template>

<script setup lang="ts">
import { ref } from 'vue';
const dateFooter = ref(new Date().getFullYear().toString());
</script>

<style scoped lang="scss">
.footer {
    background-color: $primary-color;
    padding: 2rem 1rem;

    &__container {
        @include containerWidth;
        @include flexBetween;

        p {
            color: $neutral-gray;
            font-size: 0.875rem;
        }

        a {
            color: $neutral-gray;
            transition: color 0.29s ease;

            &:hover {
                color: $background-light;
            }
        }
    }

    &__links {
        display: flex;
        gap: 1.2rem;

        a {
            font-size: 0.875rem;
            color: $neutral-gray;
            transition: color 0.29s ease;

            &:hover {
                color: $background-light;
            }
        }
    }
}

@media (max-width: 768px) {
    .footer__container {
        flex-direction: column;
        gap: 0.4rem;
    }
}
</style>
