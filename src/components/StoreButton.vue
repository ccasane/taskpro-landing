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
  flex-wrap: wrap;
  gap: 1.8rem;
  margin-top: 0.6rem;

  a {
    min-width: 170px;
    @include flexCenter;
    gap: 0.3rem;
    padding: 0.4rem 0.6rem;
    border-radius: 10px;
    border: 5px solid $neutral-gray;
    color: $background-light;
    background-color: $primary-color;
    transition:
      background-color 0.29s ease,
      box-shadow 0.29s ease;

    &:hover {
      background-color: $secondary-color;
      box-shadow: 0 2px 6px rgba($primary-color, 0.5);
    }

    span {
      display: flex;
      flex-direction: column;
      font-size: 0.75rem;

      .bold {
        font-weight: 700;
        font-size: 0.875rem;
      }
    }
  }
}

@media (max-width: 768px) {
  .hero__links {
    gap: 0.8rem;
    justify-content: center;
  }
}
</style>
