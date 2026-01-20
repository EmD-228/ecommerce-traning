<template>
    <div class="grid gap-10 items-center text-center mx-auto">
        <div class="space-y-2">
            <h2 class="text-2xl sm:text-4xl font-bold text-secondary mx-auto">Browse The Range</h2>
            <p class="text-sm sm:text-base text-secondary mx-auto">Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, quos.
            </p>
        </div>
        <div class="grid grid-cols-2 sm:grid-cols-3 gap-4 px-4 lg:px-0 justify-center ">
            <RangeItem :image="range1" itemName="Dining" />
            <RangeItem :image="range2" itemName="Living" />
            <RangeItem :image="range3" itemName="Bedroom" />
        </div>
    </div>
</template>
<script setup lang="ts">
import range1 from '../assets/images/range_1.png';
import range2 from '../assets/images/range_2.png';
import range3 from '../assets/images/range_3.png';
import RangeItem from './items/RangeItem.vue';
</script>