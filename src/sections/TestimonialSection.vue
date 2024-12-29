<template>
  <section class="testimonials">
    <div class="testimonials__container">
      <CardTestimonial
        v-for="tes in testimonials"
        :key="tes.description"
        :description="tes.description"
        :field="tes.field"
        :person="tes.person"
      ></CardTestimonial>
    </div>
  </section>
</template>

<script setup lang="ts">
import { testimonials } from '@/data/data.json';
import CardTestimonial from '@/components/CardTestimonial.vue';
</script>

<style scoped lang="scss">
.testimonials {
  padding: 5rem 1rem;
  background-color: $neutral-gray;

  &__container {
    @include containerWidth;
    @include gridCard;
  }
}
</style>
