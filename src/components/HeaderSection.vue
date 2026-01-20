<template>
    <div class="navbar bg-base-100 shadow-sm px-4">
        <div class="flex-1">
            <img src="../assets/logos/logo.png" alt="logo" class="h-5 sm:h-10 cursor-pointer">
        </div>
        <div class="hidden lg:flex md:flex-1">
            <ul class="menu menu-horizontal px-1 space-x-2 sm:space-x-8">
                <li><a href="#">Home</a></li>
                <li><a href="#">Shop</a></li>
                <li><a href="#">About</a></li>
                <li><a href="#">Contact</a></li>
            </ul>
        </div>
        <div class="hidden sm:flex flex-row gap-4">
            <UserIcon class="text-black h-6 w-6" />
            <SearchNormal1Icon class="text-black h-6 w-6" />
            <HeartIcon class="text-black h-6 w-6" />
            <ShoppingCartIcon class="text-black h-6 w-6" />
        </div>
        <Menu1Icon class="text-black sm:hidden h-6 w-6 cursor-pointer" />
    </div>
</template>
<script setup lang="ts">
import { HeartIcon, Menu1Icon, SearchNormal1Icon, ShoppingCartIcon, UserIcon } from '@placetopay/iconsax-vue/outline';
</script>
