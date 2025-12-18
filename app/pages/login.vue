<template>
    <div
        class="min-h-screen w-full flex flex-col items-center justify-center bg-[url(/photos/metraBG08black.png)] px-4">

        <!-- LOGO -->
        <img src="/photos/logo-metranet1.png" alt="MetraNet Logo" class="w-50 mb-6 drop-shadow-lg" />

        <!-- TAB WRAPPER -->
        <div class="w-full max-w-md mb-4">
            <div class="flex bg-white/10 backdrop-blur-md rounded-full p-1 border border-white/20 h-12">

                <!-- TAB EMPLOYEE -->
                <button @click="activeTab = 'employee'" :class="activeTab === 'employee'
                    ? 'bg-white text-red-600 font-semibold shadow-md'
                    : 'text-white/80'" class="flex-1 py-2 rounded-full transition">
                    Employee
                </button>

                <!-- TAB MANAGEMENT -->
                <button @click="activeTab = 'management'" :class="activeTab === 'management'
                    ? 'bg-white text-red-600 font-semibold shadow-md'
                    : 'text-white/80'" class="flex-1 py-2 rounded-full transition">
                    Management
                </button>
            </div>
        </div>

        <!-- LOGIN CARD -->
        <div class="w-full max-w-md">
            <div class="bg-white/10 backdrop-blur-md rounded-2xl p-10 shadow-2xl text-center border border-white/20">

                <!-- TITLE -->
                <h2 class="text-2xl font-bold text-white">
                    Sign in as {{ activeTab === 'employee' ? 'Employee' : 'Management' }}
                </h2>

                <p class="text-white/80 mt-2 text-sm leading-relaxed">
                    Enter your email and password to access your account<br />
                    and continue to your dashboard
                </p>

                <!-- FORM -->
                <form class="mt-8 space-y-6">

                    <!-- EMAIL -->
                    <div class="relative">
                        <input v-model="email" type="email" id="email" class="peer w-full py-3 pl-12 pr-4 rounded-lg bg-white/20 text-white
                        placeholder-transparent focus:outline-none focus:ring-2 focus:ring-white/40"
                            placeholder="Email" />

                        <!-- Floating Label -->
                        <label for="email"
                            class="absolute left-12 top-1/2 -translate-y-1/2 text-white/70 transition-all duration-300
                        peer-placeholder-shown:top-1/2 peer-placeholder-shown:text-white/70 peer-placeholder-shown:text-base
                        peer-focus:top-2 peer-focus:text-[10px] peer-focus:text-white/50 peer-not-placeholder-shown:top-2 peer-not-placeholder-shown:text-xs peer-not-placeholder-shown:text-white/0">
                            Email
                        </label>

                        <svg class="w-5 h-5 absolute left-4 top-1/2 -translate-y-1/2 text-red-100" fill="currentColor"
                            viewBox="0 0 24 24">
                            <path
                                d="M1.5 8.67v8.58a3 3 0 003 3h15a3 3 0 003-3V8.67l-8.93 5.49a3 3 0 01-3.14 0L1.5 8.67z" />
                            <path
                                d="M22.5 6.91V6.75a3 3 0 00-3-3h-15a3 3 0 00-3 3v.16l9.71 5.98a1.5 1.5 0 001.57 0L22.5 6.91z" />
                        </svg>
                    </div>

                    <!-- PASSWORD -->
                    <div class="relative">
                        <input v-model="password" :type="showPassword ? 'text' : 'password'" id="password" class="peer w-full py-3 pl-12 rounded-lg bg-white/20 text-white
                        placeholder-transparent focus:outline-none focus:ring-2 focus:ring-white/40"
                            placeholder="Password" />

                        <!-- Floating Label -->
                        <label for="password"
                            class="absolute left-12 top-1/2 -translate-y-1/2 text-white/70 transition-all duration-300
                        peer-placeholder-shown:top-1/2 peer-placeholder-shown:text-sm
                        peer-focus:top-2 peer-focus:text-[10px] peer-focus:text-white/50 peer-not-placeholder-shown:top-2 peer-not-placeholder-shown:text-xs peer-not-placeholder-shown:text-white/0">
                            Password
                        </label>

                        <!-- ICON (LEFT) -->
                        <svg class="w-5 h-5 absolute left-4 top-1/2 -translate-y-1/2 text-red-100" fill="currentColor"
                            viewBox="0 0 24 24">
                            <path fill-rule="evenodd" clip-rule="evenodd"
                                d="M12 1.5a5.25 5.25 0 00-5.25 5.25v3a3 3 0 00-3 3v6.75a3 3 0 003 3h10.5a3 3 0 003-3v-6.75a3 3 0 00-3-3v-3c0-2.9-2.35-5.25-5.25-5.25zm3.75 8.25v-3a3.75 3.75 0 10-7.5 0v3h7.5z" />
                        </svg>

                        <!-- SHOW/HIDE BUTTON -->
                        <button type="button" @click="showPassword = !showPassword"
                            class="absolute right-4 top-1/2 -translate-y-1/2 text-white/70">

                            <!-- EYE OPEN -->
                            <svg v-if="showPassword" data-slot="icon" fill="none" stroke-width="1.5"
                                stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"
                                class="w-5 h-5" aria-hidden="true">
                                <path stroke-linecap="round" stroke-linejoin="round"
                                    d="M2.036 12.322a1.012 1.012 0 0 1 0-.639C3.423 7.51 7.36 4.5 12 4.5c4.638 0 8.573 3.007 9.963 7.178.07.207.07.431 0 .639C20.577 16.49 16.64 19.5 12 19.5c-4.638 0-8.573-3.007-9.963-7.178Z" />
                                <path stroke-linecap="round" stroke-linejoin="round"
                                    d="M15 12a3 3 0 1 1-6 0 3 3 0 0 1 6 0Z" />
                            </svg>

                            <!-- EYE SLASH -->
                            <svg v-else data-slot="icon" fill="none" stroke-width="1.5" stroke="currentColor"
                                viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg" class="w-5 h-5"
                                aria-hidden="true">
                                <path stroke-linecap="round" stroke-linejoin="round"
                                    d="M3.98 8.223A10.477 10.477 0 0 0 1.934 12C3.226 16.338 7.244 19.5 12 19.5c.993 0 1.953-.138 2.863-.395M6.228 6.228A10.451 10.451 0 0 1 12 4.5c4.756 0 8.773 3.162 10.065 7.498a10.522 10.522 0 0 1-4.293 5.774M6.228 6.228 3 3m3.228 3.228 3.65 3.65m7.894 7.894L21 21m-3.228-3.228-3.65-3.65m0 0a3 3 0 1 0-4.243-4.243m4.242 4.242L9.88 9.88" />
                            </svg>
                        </button>
                    </div>

                    <div class="flex justify-end">
                        <NuxtLink to="/forgot" class="text-white/90 text-xs hover:underline">
                            Forgot Password?
                        </NuxtLink>
                    </div>

                    <!-- BUTTON -->
                    <div class="mt-8 flex justify-center">
                        <NuxtLink :to="activeTab === 'employee' ? '/employee/dashboard' : '/management/dashboard'"
                            class="w-full px-12 py-3 rounded-lg bg-[#B10000] hover:bg-[#8A0000] text-white font-semibold transition shadow-xl text-center">
                            Get Started
                        </NuxtLink>
                    </div>
                </form>

                <p class="text-center text-xs text-gray-300 mt-8">
                    © 2025 PT. Metranet — All Rights Reserved
                </p>

            </div>
        </div>

    </div>
</template>

<script setup>
const activeTab = ref("employee")

const email = ref("")
const password = ref("")
const showPassword = ref(false)

definePageMeta({ layout: false })
</script>
