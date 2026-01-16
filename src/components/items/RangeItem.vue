<template>
    <div class="space-y-4 justify-center items-center">
        <img :src="image" alt="range-item" class="w-full max-h-78 object-cover rounded-lg">
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