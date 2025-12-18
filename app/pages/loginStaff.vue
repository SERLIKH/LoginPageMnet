<template>
  <!-- LOGIN BOX -->
  <div class="bg-white/10 backdrop-blur-lg rounded-2xl p-10 shadow-2xl text-center border border-white/20">
    <!-- TITLE -->
    <h2 class="text-2xl font-bold text-white">Sign in as Management</h2>
    <p class="text-white/80 mt-2 text-sm leading-relaxed">
      Enter your email and password to access your account<br />
      and continue to your dashboard
    </p>

    <!-- FORM -->
    <form class="mt-8 space-y-6">
      <!-- EMAIL INPUT -->
      <div class="relative">
        <img src="/icon/mail.png" class="w-5 h-5 absolute left-4 top-1/2 -translate-y-1/2 brightness-80"/>
        <input type="email" placeholder="Email" class="w-full py-3 pl-12 pr-4 rounded-lg bg-white/20 text-white placeholder-white/70 focus:outline-none focus:ring-2 focus:ring-white/40"/>
      </div>

      <!-- PASSWORD INPUT -->
      <div class="relative">
        <img src="/icon/lock.png" class="w-5 h-5 absolute left-4 top-1/3 -translate-y-1/2 brightness-80"/>
        <input type="password" placeholder="Password" class="w-full py-3 pl-12 pr-4 rounded-lg bg-white/20 text-white placeholder-white/70 focus:outline-none focus:ring-2 focus:ring-white/40"/>
        <div class="flex justify-end mt-1">
          <NuxtLink to="/forgot" class="text-white/90 text-xs hover:underline">
            Forgot Password?
          </NuxtLink>
        </div>
      </div>

      <!-- BUTTON -->
      <div class="mt-8 flex justify-center">
        <NuxtLink to="/enter" class="w-full px-12 py-3 rounded-lg bg-[#B10000] hover:bg-[#8A0000]
        text-white font-semibold transition shadow-xl text-center">
          Get Started
        </NuxtLink>
      </div>
    </form>

    <SocialButton />
  </div>  
</template>

