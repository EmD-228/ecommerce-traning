<template>
    <div class="space-y-4">
        <div class="w-full ">
            <img :src="image" alt="range-item" class="object-cover rounded-lg">
        </div>
        <h3 class="text-xl font-medium text-secondary">{{ itemName }}</h3>
    </div>
</template>
<script setup lang="ts">
interface Props {
    image: string;
    itemName: string;
}

const { image, itemName } = defineProps<Props>();
</script>