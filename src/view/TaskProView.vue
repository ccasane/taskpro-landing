<template>
    <HeaderApp></HeaderApp>
    <main>
        <HeroSection></HeroSection>
        <BenefitSection></BenefitSection>
        <TestimonialSection></TestimonialSection>
        <StoreSection></StoreSection>
    </main>
    <FooterApp></FooterApp>
</template>
<script setup lang="ts">
import HeaderApp from '@/components/HeaderApp.vue';
import HeroSection from '@/sections/HeroSection.vue';
import BenefitSection from '@/sections/BenefitSection.vue';
import TestimonialSection from '@/sections/TestimonialSection.vue';
import StoreSection from '@/sections/StoreSection.vue';
import FooterApp from '@/components/FooterApp.vue';
</script>
