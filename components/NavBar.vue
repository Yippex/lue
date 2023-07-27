<script setup>
  import { ref } from 'vue';

  const isMenuOpen = ref(false);

  function toggleMenu() {
    isMenuOpen.value = !isMenuOpen.value;
  }
</script>

<template>
  <div class="w-full  ">
    <div class="flex items-center justify-between h-20 md:px-24 px-4 ">
      <div>
        <NuxtLink to="/">
          <img src="../assets/logo-black.24eb56ae.png" alt="" class="h-8">
        </NuxtLink>
      </div>
      <div class="lg:hidden">
        <button @click="toggleMenu">
          <!-- Replace the `hamburger-icon.png` with your hamburger icon -->
          <img src="../assets/hamburger.svg" alt="Menu" class="h-8">
        </button>
      </div>
      <nav class="hidden lg:flex items-center gap-20">
        <NuxtLink to="/about" class="hover:text-[#ffa440]">About</NuxtLink>
        <NuxtLink to="/about" class="hover:text-[#ffa440]">Blog</NuxtLink>
        <NuxtLink to="/about" class="hover:text-[#ffa440]">Contact</NuxtLink>
        <NuxtLink to="/about" class="bg-[#ffa440] text-white p-2 rounded-md w-20 text-center">Login</NuxtLink>
      </nav>
    </div>

    <!-- Hamburger menu -->
    <div v-if="isMenuOpen" class="lg:hidden absolute top-20 left-0 w-full bg-white z-40 shadow">
      <div class="flex flex-col gap-4 p-4">
        <NuxtLink to="/about" class="hover:text-[#ffa440]">About</NuxtLink>
        <NuxtLink to="/about" class="hover:text-[#ffa440]">Blog</NuxtLink>
        <NuxtLink to="/about" class="hover:text-[#ffa440]">Contact</NuxtLink>
        <NuxtLink to="/about" class="bg-[#ffa440] text-white p-2 rounded-md w-20 text-center">Login</NuxtLink>
      </div>
    </div>
  </div>
</template>
