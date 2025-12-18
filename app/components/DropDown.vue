<template>
  <div class="w-full">
    <select
      v-model="selectedRole"
      class="w-full bg-white/10 text-white px-4 py-3 rounded-xl backdrop-blur-lg border border-white/20 shadow-2xl focus:outline-none focus:ring-2 focus:ring-white/30"
    >
      <option disabled value="">Sign in as..</option>
      <option v-for="role in roles" :key="role" :value="role" class="text-black">
        {{ role }}
      </option>
    </select>
  </div>
</template>

<script setup>
import { ref, watch, onMounted } from 'vue'
import { useRouter, useRoute } from 'vue-router'

const router = useRouter()
const route = useRoute()

const roles = ['Employee', 'Management']
const selectedRole = ref('')

// ✅ Set default sesuai halaman
onMounted(() => {
  if (route.path === '/loginStaff') {
    selectedRole.value = 'Management'
  } else {
    selectedRole.value = 'Employee'
  }
})

// ✅ Redirect kalau berubah
watch(selectedRole, (newRole) => {
  if (newRole === 'Management' && route.path !== '/loginStaff') {
    router.push('/loginStaff')
  } else if (newRole === 'Employee' && route.path !== '/') {
    router.push('/')
  }
})
</script>
