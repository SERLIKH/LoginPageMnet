<template>
    <div class="min-h-screen w-full flex items-center justify-center relative overflow-hidden">

        <!-- BACKGROUND IMAGE -->
        <img src="/photos/metraBG08.png" class="absolute inset-0 w-full h-full object-cover opacity-90" />

        <!-- COLOR OVERLAY -->
        <div class="absolute inset-0 bg-gradient-to-br from-[#F8091E]/10 to-[#000]/60"></div>

        <!-- CONTENT WRAPPER -->
        <div
            class="relative z-10 w-full max-w-5xl mx-auto flex flex-col md:flex-row items-start md:items-center px-6 md:px-12 py-16 gap-10">

            <!-- LEFT SECTION -->
            <div class="text-white flex-1">
                <img src="/photos/logo-metranet1.png" alt="MetraNet" class="h-12 mb-10">

                <h1 class="text-4xl md:text-5xl font-bold leading-tight">
                    Login<br />
                    <span class="text-[#fff]">as {{ activeTab }}.</span>
                </h1>

                <p class="mt-4 text-white/70">
                    Forgot your password?
                    <NuxtLink class="text-[#F8091E] font-medium hover:underline" to="#">
                        Here
                    </NuxtLink>
                </p>
            </div>

            <!-- RIGHT (FORM PANEL) -->
            <div class="w-full md:w-[420px]">

                <!-- TABS -->
                <div class="flex mb-6 bg-white/10 rounded-xl overflow-hidden border border-white/20">
                    <button @click="activeTab = 'Employee'" :class="[
                        'w-1/2 py-3 font-semibold transition',
                        activeTab === 'Employee'
                            ? 'bg-gradient-to-r from-[#A9085A] to-[#F8091E] text-white'
                            : 'text-white/70 hover:bg-white/10'
                    ]">
                        Employee
                    </button>

                    <button @click="activeTab = 'Management'" :class="[
                        'w-1/2 py-3 font-semibold transition',
                        activeTab === 'Management'
                            ? 'bg-gradient-to-r from-[#A9085A] to-[#F8091E] text-white'
                            : 'text-white/70 hover:bg-white/10'
                    ]">
                        Management
                    </button>
                </div>

                <!-- FORM -->
                <form
                    class="bg-[#fff]/10 backdrop-blur-md rounded-2xl p-8 shadow-xl border border-white/10 space-y-4 text-white">

                    <div>
                        <label class="form-label">Email</label>
                        <input type="email" placeholder="example@metranet.co.id"
                            class="form-input p-2 my-3 w-full rounded-md bg-white/20 text-white placeholder-white/70 focus:outline-none focus:ring-2 focus:ring-white/40" />
                    </div>

                    <div>
                        <label class="form-label">Password</label>
                        <input type="password" placeholder="••••••••"
                            class="form-input p-2 my-3 w-full rounded-md bg-white/20 text-white placeholder-white/70 focus:outline-none focus:ring-2 focus:ring-white/40" />
                    </div>

                    <!-- BUTTON -->
                    <div class="flex items-center pt-4">
                        <button type="submit"
                            class="w-full py-3 rounded-xl bg-gradient-to-r from-[#A9085A] to-[#F8091E] hover:opacity-60 text-white font-semibold shadow-lg shadow-[#F8091E]/30 transition">
                            Login
                        </button>
                    </div>

                    <p class="text-center text-xs text-gray-300 mt-8">
                        © 2025 PT. Metranet — All Rights Reserved
                    </p>
                </form>
            </div>
        </div>
    </div>
</template>

<script setup>
definePageMeta({ layout: false })
import { ref } from 'vue'

const activeTab = ref("Employee")   // Default tab
</script>
