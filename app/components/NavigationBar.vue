<template>
  <header class="bg-gradient-to-r from-[#F8091E] to-[#A9085A]">
    <div class="fixed flex items-center justify-between w-full px-4 py-4 border-b-1 border-white/20">

      <!-- LOGO -->
      <div>
        <NuxtLink to="/" class="text-xl font-bold">
            <img src="/icon/flying.png" alt="logo" class="w-full h-10 object-cover"/>
        </NuxtLink>
      </div>

      <!-- NAV MENU -->
      <nav class="hidden md:flex items-center gap-6 font-medium">
        <NuxtLink to="/" class="text-white hover:text-red-400 transition">Home</NuxtLink>
        <NuxtLink to="/" class="text-white hover:text-red-400 transition">Company</NuxtLink>
        <NuxtLink to="/" class="text-white hover:text-red-400 transition">Business</NuxtLink>
        <NuxtLink to="/" class="text-white hover:text-red-400 transition">ESG</NuxtLink>
        <NuxtLink to="/" class="text-white hover:text-red-400 transition">News</NuxtLink>
        <NuxtLink to="/" class="text-white hover:text-red-400 transition">Careers</NuxtLink>
        <NuxtLink to="/" class="text-white hover:text-red-400 transition">Contact</NuxtLink>
      </nav>

      <!-- SEARCH BAR -->
      <div class="hidden md:block">
        <img src="/icon/metranet.png" alt="logo" class="w-full h-10 object-cover"/>
      </div>
    </div>
  </header>
</template>