<template>
    <div class="grid grid-cols-3 gap-8 items-center text-center bg-accent py-5">
        <div class="mx-22 text-left space-y-4">
            <h2 class="text-4xl font-bold text-secondary mx-auto">50+ Beautiful rooms inspiration</h2>
            <p class="text-secondary mx-auto">Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, quos.
            </p>
            <div class="bg-primary text-primary-content text-center py-2 px-10 max-w-fit font-medium">Explore More</div>


        </div>
        <div class="relative">
            <img src="../assets/images/room_1.png" alt="rooms-image" class="max-w-full object-cover max-h-100">
            <div class="absolute bottom-4 left-4 flex justify-end">
                <div class=" bg-white opacity-80 p-6">
                    <div class="text-center">
                        <p class="text-secondary text-xs">01 ---- Bed Room</p>
                        <h3 class="text-xl font-bold text-secondary">Inner Peace</h3>
                    </div>
                </div>
                <div class="bg-primary py-4 px-4 max-w-fit max-h-fit self-end ">
                    <ArrowRight1Icon class="text-white h-6 w-6" />
                </div>
            </div>
        </div>
        <div class="relative space-y-4">
            <div class="carousel carousel-center max-w-full space-x-4  ">
                <div class="absolute right-5 top-1/2 flex -translate-y-1/2 transform justify-between">
                    <a href="#slide2" class="btn btn-circle text-primary">❯</a>
                </div>
                <div class="carousel-item">
                    <img src="https://img.daisyui.com/images/stock/photo-1559703248-dcaaec9fab78.webp" class="" />
                </div>
                <div class="carousel-item">
                    <img src="https://img.daisyui.com/images/stock/photo-1565098772267-60af42b81ef2.webp" class="" />
                </div>
                <div class="carousel-item">
                    <img src="https://img.daisyui.com/images/stock/photo-1572635148818-ef6fd45eb394.webp" class="" />
                </div>

            </div>
            <div class="flex justify-start items-center gap-2 py-2">
                <input type="radio" name="radio-2" class="radio radio-sm radio-primary" :checked="true" />
                <input type="radio" name="radio-2" class="radio radio-sm radio-primary" :checked="true" />
                <input type="radio" name="radio-2" class="radio radio-sm radio-primary" :checked="true" />
                <input type="radio" name="radio-2" class="radio radio-sm radio-primary" :checked="true" />
            </div>
        </div>


    </div>
</template>
<script setup lang="ts">
import { ArrowRight1Icon } from '@placetopay/iconsax-vue/outline';
</script>