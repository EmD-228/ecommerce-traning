<template>
    <div class="justify-center items-center bg-base-100">
        <div class="relative">
            <img :src="image" :alt="itemName" class="w-full max-h-78 object-cover">
            <div class="absolute top-4 right-4 flex justify-end">
                <div class=" bg-white opacity-80 h-10 w-10 rounded-full text-center flex items-center justify-center">
                    <h3 class="text-xs font-bold text-secondary">New</h3>
                </div>
            </div>
        </div>
        <div class="space-y-1 px-4 py-6 text-left">
            <h3 class="text-xl font-medium text-secondary">{{ itemName }}</h3>
            <p class="text-xs text-secondary">{{ itemDescription }}</p>
            <div class="flex flex-row gap-2">
                <span class="text-sm font-medium text-secondary">Rp {{ formatPrice(itemPrice) }}</span>
                <span v-if="itemOldPrice" class="text-sm line-through text-gray-400">Rp {{ formatPrice(itemOldPrice) }}</span>
            </div>
        </div>
    </div>
</template>
<script setup lang="ts">
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
</script>
