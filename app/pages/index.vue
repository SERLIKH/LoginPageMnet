<template>
  <div
    class="min-h-screen w-full flex flex-col items-center justify-center bg-[url(/photos/gradientBG.png)] px-4 space-y-6">
    <div class="w-full max-w-md">
      <!-- LOGIN BOX -->
      <div class="bg-white/10 backdrop-blur-lg rounded-2xl p-10 shadow-2xl text-center border border-white/20">
        <!-- TITLE -->
        <h2 class="text-2xl font-bold text-white">Sign in as Employee</h2>
        <p class="text-white/80 mt-2 text-sm leading-relaxed">
          Enter your email and password to access your account<br />
          and continue to your dashboard
        </p>

        <!-- FORM -->
        <form class="mt-8 space-y-6">
          <!-- EMAIL INPUT -->
          <div class="relative">
            <svg class="w-5 h-5 absolute left-4 top-1/2 -translate-y-1/2 text-red-200" data-slot="icon"
              fill="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
              <path d="M1.5 8.67v8.58a3 3 0 0 0 3 3h15a3 3 0 0 0 3-3V8.67l-8.928 5.493a3 3 0 0 1-3.144 0L1.5 8.67Z">
              </path>
              <path
                d="M22.5 6.908V6.75a3 3 0 0 0-3-3h-15a3 3 0 0 0-3 3v.158l9.714 5.978a1.5 1.5 0 0 0 1.572 0L22.5 6.908Z">
              </path>
            </svg>
            <input type="email" placeholder="Email"
              class="w-full py-3 pl-12 pr-4 rounded-lg bg-white/20 text-white placeholder-white/70 focus:outline-none focus:ring-2 focus:ring-white/40" />
          </div>

          <!-- PASSWORD INPUT -->
          <div class="relative">
            <svg class="w-5 h-5 absolute left-4 top-1/3 -translate-y-1/2 text-red-200" data-slot="icon"
              fill="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
              <path clip-rule="evenodd" fill-rule="evenodd"
                d="M12 1.5a5.25 5.25 0 0 0-5.25 5.25v3a3 3 0 0 0-3 3v6.75a3 3 0 0 0 3 3h10.5a3 3 0 0 0 3-3v-6.75a3 3 0 0 0-3-3v-3c0-2.9-2.35-5.25-5.25-5.25Zm3.75 8.25v-3a3.75 3.75 0 1 0-7.5 0v3h7.5Z">
              </path>
            </svg>
            <input type="password" placeholder="Password"
              class="w-full py-3 pl-12 pr-4 rounded-lg bg-white/20 text-white placeholder-white/70 focus:outline-none focus:ring-2 focus:ring-white/40" />
            <div class="flex justify-end mt-1">
              <NuxtLink to="/forgot" class="text-white/90 text-xs hover:underline">
                Forgot Password?
              </NuxtLink>
            </div>
          </div>

          <!-- BUTTON -->
          <div class="mt-8 flex justify-center">
            <NuxtLink to="/enter"
              class="w-full px-12 py-3 rounded-lg bg-[#B10000] hover:bg-[#8A0000] text-white font-semibold transition shadow-xl text-center">
              Get Started
            </NuxtLink>
          </div>
        </form>

        <!-- <SocialButton /> -->
      </div>
    </div>
  </div>
</template>



<script setup>
definePageMeta({
  layout: false
})
</script>