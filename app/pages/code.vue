<template>
  <!-- LOGIN BOX -->
  <div class="bg-white/10 backdrop-blur-lg rounded-2xl p-10 shadow-2xl text-center border border-white/20">
    <!-- TITLE -->
    <h2 class="text-2xl font-bold text-white">Verification Code</h2>
    <p class="text-white/80 mt-2 text-sm leading-relaxed">
      Please enter the verification code to confirm your identity.
    </p>

    <!-- OTP INPUTS -->
    <div class="flex justify-center gap-4 mt-8">
      <div v-for="n in 4" :key="n"
        class="w-16 h-10 bg-white/30 backdrop-blur-lg rounded-xl flex items-center justify-center">
        <input maxlength="1"
          class="w-full h-10 bg-transparent text-center text-2xl font-semibold text-white focus:outline-none" />
      </div>
    </div>

    <!-- VERIFY BUTTON -->
    <div class="mt-8 flex justify-center">
      <NuxtLink to="/password"
        class="w-full px-12 py-3 rounded-lg bg-[#B10000] hover:bg-[#8A0000] text-white font-semibold transition shadow-xl text-center">
        Verify
      </NuxtLink>
    </div>

    <!-- SOCIAL LOGIN -->
    <SocialButton />
  </div>
</template>
