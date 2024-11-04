<template>
  <section class="store">
    <div class="store__container">
      <h2>{{ store.title }}</h2>
      <p>{{ store.description[0] }}</p>
      <p>{{ store.description[1] }}</p>
      <StoreButton></StoreButton>
    </div>
  </section>
</template>

<script setup lang="ts">
import { store } from '@/data/data.json';
import StoreButton from '@/components/StoreButton.vue';
</script>

<style scoped lang="scss">
.store {
  background-color: $background-light;
  padding: 4rem 1rem;

  &__container {
    @include containerWidth;
    @include flexColunm;
  }

  h2 {
    max-width: 700px;
    font-size: 2.5rem;
    line-height: 1.1;
    font-weight: 800;
    text-align: center;
    color: $primary-color;
  }

  p {
    max-width: 550px;
    margin: 0.6rem 0;
    font-size: 1.125rem;
    color: $secondary-color;
    text-align: center;
  }
}

@media (max-width: 768px) {
  .store__container {
    h2 {
      font-size: 2rem;
    }

    p {
      font-size: 1rem;
    }
  }
}
</style>
