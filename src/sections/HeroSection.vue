<template>
  <section class="hero">
    <div class="hero__container">
      <div class="hero__data">
        <h1>
          {{ hero.title }}
        </h1>
        <p>
          {{ hero.description[0] }}
        </p>
        <p>
          {{ hero.description[1] }}
        </p>
        <HeroButtons></HeroButtons>
      </div>
      <HeroImage></HeroImage>
    </div>
  </section>
</template>

<script setup lang="ts">
import { hero } from '@/data/data.json';
import HeroImage from '@/components/HeroImage.vue';
import HeroButtons from '@/components/HeroButtons.vue';
</script>

<style scoped lang="scss">
.hero {
  @include flexCenter;
  padding: 5rem 1rem;
  background-color: $background-light;

  &__container {
    @include containerWidth;
    @include flexBetween;
  }

  &__data {
    max-width: 500px;
    width: 100%;
    h1 {
      font-size: 3.4rem;
      line-height: 1.1;
      color: $primary-color;
      font-weight: 800;
    }
    p {
      max-width: 480px;
      width: 100%;
      margin: 1rem 0;
      font-size: 1.125rem;
      color: $secondary-color;
    }
  }
}

@media (max-width: 768px) {
  .hero {
    .hero__data {
      h1 {
        font-size: 2rem;
      }
      p {
        font-size: 1rem;
      }
    }
  }
}
</style>
