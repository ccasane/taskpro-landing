<template>
  <div class="card">
    <div class="card__header">
      <img :src="getIcon(icon)" :alt="alt" />
    </div>
    <h3>{{ title }}</h3>
    <p>{{ description }}</p>
  </div>
</template>

<script setup lang="ts">
import FirstIcon from '@/assets/icons/first-icon.svg';
import SecondIcon from '@/assets/icons/second-icon.svg';
import ThirdIcon from '@/assets/icons/third-icon.svg';
import FordIcon from '@/assets/icons/ford-icon.svg';

type IconKey = 'first-icon' | 'second-icon' | 'third-icon' | 'ford-icon';

const icons: Record<IconKey, string> = {
  'first-icon': FirstIcon,
  'second-icon': SecondIcon,
  'third-icon': ThirdIcon,
  'ford-icon': FordIcon,
};
const getIcon = (iconKey: IconKey): string => icons[iconKey];

defineProps<{
  title: string;
  description: string;
  icon: IconKey;
  alt: string;
}>();
</script>

<style scoped lang="scss">
.card {
  text-align: center;
  &__header {
    @include flexCenter;
    margin: 0 auto 0.4rem;
  }

  h3 {
    font-size: 1rem;
    margin-bottom: 0.4rem;
    color: $background-light;
  }

  p {
    color: $neutral-gray;
  }
}
</style>
