<template>
    <div class="flex flex-col sm:flex-row gap-8 items-center text-center bg-accent py-5">
        <div class="flex-1 mx-4 sm:mx-8 lg:mx-22 text-left space-y-4">
            <h2 class="text-2xl sm:text-4xl font-bold text-secondary mx-auto">50+ Beautiful rooms inspiration</h2>
            <p class="text-secondary mx-auto">Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, quos.
            </p>
            <div class="bg-primary text-primary-content text-center py-2 px-10 max-w-fit font-medium">Explore More</div>


        </div>
        <div class="relative sm:flex-1 mx-1 sm:mx-0">

            <div class="max-w-full mx-4 sm:mx-0 ">
                <img src="../assets/images/room_1.png" alt="rooms-image" class="object-cover">
            </div>
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
        <div class="relative flex-1 space-y-4 mx-4 sm:mx-0">
            <div class="carousel carousel-center max-w-full space-x-4  ">
                <div class="hidden sm:block absolute right-5 top-1/2 -translate-y-1/2 transform justify-between">
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