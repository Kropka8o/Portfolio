<template >
  <div class="min-h-screen grid grid-cols-1 grid-rows-[auto_1fr_auto] gap-0">
    <div>
      <header>
        <Header />
    </header>
    </div>
    <div
        :style="{'background-color': '#FEECF6'}"
        class="py-5"
    >
      <div class="wrapper flex justify-center items-center">
        <nuxt-page />
      </div>
    </div>
    <div class="">
      <footer class="bg-pink-200">
        <Footer />
      </footer>
    </div>
  </div>
</template>
<script setup lang="ts">
</script>