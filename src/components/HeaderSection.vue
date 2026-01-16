<template>
    <div class="navbar bg-base-100 shadow-sm px-8">
        <div class="flex-1">
            <img src="../assets/logos/logo.png" alt="logo" class="h-10">
        </div>
        <div class="flex-1">
            <ul class="menu menu-horizontal px-1 space-x-8">
                <li><a href="#">Home</a></li>
                <li><a href="#">Shop</a></li>
                <li><a href="#">About</a></li>
                <li><a href="#">Contact</a></li>
            </ul>
        </div>
        <div class="flex flex-row gap-4">
            <UserIcon class="text-black h-6 w-6" />
            <SearchNormal1Icon class="text-black h-6 w-6" />
            <HeartIcon class="text-black h-6 w-6" />
            <ShoppingCartIcon class="text-black h-6 w-6" />
        </div>
    </div>
</template>
<script setup lang="ts">
import { HeartIcon, SearchNormal1Icon, ShoppingCartIcon, UserIcon } from '@placetopay/iconsax-vue/outline';
</script>
