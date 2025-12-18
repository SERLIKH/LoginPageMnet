<template>
  <!-- LOGIN BOX -->
  <div class="bg-white/10 backdrop-blur-lg rounded-2xl p-10 shadow-2xl text-center border border-white/20">
    <!-- TITLE -->
    <h2 class="text-2xl font-bold text-white">Reset password</h2>
    <p class="text-white/80 mt-2 text-sm leading-relaxed">
      Please enter your email to receive a verification code
    </p>

    <!-- FORM -->
    <form class="mt-8 space-y-6">
      <!-- EMAIL INPUT -->
      <div class="relative">
        <img src="/icon/mail.png" class="w-5 h-5 absolute left-4 top-1/2 -translate-y-1/2 brightness-80" />
        <input type="email" placeholder="Email"
          class="w-full py-3 pl-12 pr-4 rounded-lg bg-white/20 text-white placeholder-white/70 focus:outline-none focus:ring-2 focus:ring-white/40" />
      </div>

      <!-- BUTTON -->
      <div class="mt-8 flex justify-center">
        <NuxtLink to="/code"
          class="w-full px-12 py-3 rounded-lg bg-[#B10000] hover:bg-[#8A0000] text-white font-semibold transition shadow-xl text-center">
          Send
        </NuxtLink>
      </div>
    </form>

    <!-- SIGN IN AS STAFF -->
    <div class="mt-1">
      <NuxtLink class="text-white/80 text-sm hover:underline" to="/">
        Sign in as guest
      </NuxtLink>
    </div>

    <!-- SOCIAL LOGIN BUTTONS -->
    <SocialButton />
  </div>
</template>
