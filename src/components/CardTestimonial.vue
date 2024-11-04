<template>
  <div class="card">
    <div class="card__header">
      <p>{{ description }}</p>
    </div>
    <div class="card__footer">
      <p>{{ person }}</p>
      <span>{{ field }}</span>
    </div>
  </div>
</template>

<script setup lang="ts">
defineProps<{
  description: string;
  person: string;
  field: string;
}>();
</script>

<style scoped lang="scss">
.card {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  color: $primary-color;
  background-color: $background-light;

  &__header {
    padding: 1rem;
  }

  &__footer {
    padding: 0.6rem 1rem;
    background-color: $secondary-color;
    color: $background-light;

    p {
      font-weight: 700;
    }

    span {
      font-size: 0.875rem;
    }
  }
}
</style>
