<template>
  <!-- NAVBAR -->
  <NavigationBar />

  <div
    class="min-h-screen w-full flex flex-col items-center justify-center bg-[url(/photos/gradientBG.png)] px-4 space-y-6">
    <!-- DROPDOWN -->
    <div class="w-full max-w-md">
      <DropDown />
    </div>

    <!-- MAIN CONTENT -->
    <div class="w-full max-w-md">
      <slot />
    </div>
  </div>
</template>