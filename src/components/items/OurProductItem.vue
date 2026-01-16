<template>
    <div @mouseenter="handleHover" @mouseleave="handleHover" class="justify-center items-center bg-base-100 relative transition-all duration-300">
        <div class="relative">
            <img :src="image" :alt="itemName" class="w-full max-h-78 object-cover">
            <div class="absolute top-4 right-4 flex justify-end">
                <div
                    class=" bg-green-900 opacity-80 h-10 w-10 rounded-full text-center flex items-center justify-center">
                    <h3 class="text-xs font-bold text-white">New</h3>
                </div>
            </div>
        </div>
        <div class="space-y-1 px-4 py-6 text-left">
            <h3 class="text-xl font-medium text-secondary">{{ itemName }}</h3>
            <p class="text-xs text-secondary">{{ itemDescription }}</p>
            <div class="flex flex-row gap-2">
                <span class="text-sm font-medium text-secondary">Rp {{ formatPrice(itemPrice) }}</span>
                <span v-if="itemOldPrice" class="text-sm line-through text-gray-400">Rp {{ formatPrice(itemOldPrice)
                }}</span>
            </div>
        </div>
        <div v-if="isHover" class="absolute bottom-0 left-0 right-0 top-0 w-full h-full bg-black/40 p-6 flex flex-col items-center justify-center gap-4">
            <div
                class="text-primary bg-white hover:text-primary-content hover:bg-primary cursor-pointer transition-all duration-300 text-center py-2 px-10 max-w-fit font-medium mx-auto">
                Add To Cart</div>
            <div class="text-center flex flex-row gap-4 items-center justify-center">
                <div class="flex flex-row gap-2 items-center justify-center cursor-pointer">
                    <Hierarchy3Icon class="text-[#ffffff] h-4 w-4" />
                    <span class="text-white text-xs">Share</span>
                </div>
                <div class="flex flex-row gap-2 items-center justify-center cursor-pointer">
                    <Arrow2Icon class="text-[#ffffff] h-4 w-4" />
                    <span class="text-white text-xs">Compare</span>
                </div>
                <div class="flex flex-row gap-2 items-center justify-center cursor-pointer">
                    <HeartIcon class="text-[#ffffff] h-4 w-4" />
                    <span class="text-white text-xs">Like</span>
                </div>

            </div>

        </div>
    </div>
</template>
<script setup lang="ts">
import { Arrow2Icon, HeartIcon, Hierarchy3Icon } from '@placetopay/iconsax-vue/outline';
import { ref } from 'vue';
const isHover = ref(false);
interface Props {
    image: string;
    itemName: string;
    itemDescription: string;
    itemPrice: number;
    itemOldPrice: number | undefined;
}

const { image, itemName, itemDescription, itemPrice, itemOldPrice } = defineProps<Props>();

const formatPrice = (price: number): string => {
    return price.toString().replace(/\B(?=(\d{3})+(?!\d))/g, ".");
};
const handleHover = () => {
    isHover.value = !isHover.value;
};
</script>
