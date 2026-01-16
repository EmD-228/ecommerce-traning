<script setup lang="ts">
import FooterSection from './components/FooterSection.vue';
import FurnitureSection from './components/FurnitureSection.vue';
import HeaderSection from './components/HeaderSection.vue';
import HeroSection from './components/HeroSection.vue';
import OurProducts from './components/OurProducts.vue';
import RangeSection from './components/RangeSection.vue';
import RoomsSection from './components/RoomsSection.vue';
</script>

<template>
  <HeaderSection />
  <section class="grid gap-10 pb-10">
    <HeroSection />
    <RangeSection />
    <OurProducts />
    <RoomsSection />
    <FurnitureSection />
    <FooterSection />
  </section>
</template>

<style scoped></style>
