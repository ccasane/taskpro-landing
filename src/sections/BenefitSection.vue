<template>
  <section class="benefits">
    <div class="benefits__container">
      <BenefitCard
        v-for="ben in benefits"
        :key="ben.title"
        :icon="ben.icon"
        :alt="ben.alt"
        :title="ben.title"
        :description="ben.description"
      />
    </div>
  </section>
</template>

<script setup lang="ts">
import { benefits as rawBenefits } from '@/data/data.json';
import BenefitCard from '@/components/BenefitCard.vue';

type IconKey = 'first-icon' | 'second-icon' | 'third-icon' | 'ford-icon';

type Benefit = {
  title: string;
  description: string;
  icon: IconKey;
  alt: string;
};

const benefits: Benefit[] = rawBenefits as Benefit[];
</script>

<style scoped lang="scss">
.benefits {
  padding: 4rem 1rem;
  background-color: $secondary-color;

  &__container {
    @include gridCard;
    @include containerWidth;
  }
}
</style>
