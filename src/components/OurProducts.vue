<template>
    <div class="grid gap-4 items-center text-center mx-auto max-w-7xl">

        <h2 class="text-2xl sm:text-4xl font-bold text-secondary mx-auto">Our Products</h2>
        <div class="grid grid-cols-2 sm:grid-cols-3 lg:grid-cols-4 gap-4 sm:gap-6 px-4 lg:px-0 place-items-stretch">
            <OurProductItem v-for="product in products" :key="product.id" :image="getImageUrl(product.image)"
                :itemName="product.itemName" :itemDescription="product.itemDescription" :itemPrice="product.itemPrice"
                :itemOldPrice="product.itemOldPrice" />

        </div>
        <div class="text-primary hover:border-green-900 hover:text-green-900 cursor-pointer transition-all duration-300 text-center py-2 px-10 max-w-fit font-medium border border-primary mx-auto">
            Show More</div>


    </div>
</template>
<script setup lang="ts">
import data from '../assets/data/data.json';
import range1 from '../assets/images/range_1.png';
import range2 from '../assets/images/range_2.png';
import range3 from '../assets/images/range_3.png';
import room1 from '../assets/images/room_1.png';
import room2 from '../assets/images/room_2.png';
import room3 from '../assets/images/room_3.png';
import OurProductItem from './items/OurProductItem.vue';

const products = data.products;

const imageMap: Record<string, string> = {
    'range_1': range1,
    'range_2': range2,
    'range_3': range3,
    'room_1': room1,
    'room_2': room2,
    'room_3': room3,
};

const getImageUrl = (imageKey: string): string => {
    return imageMap[imageKey] || range1;
};
</script>