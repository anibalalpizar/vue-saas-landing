<script setup lang="ts">
const companies = [
  {
    name: "Accenture",
    logo: "https://upload.wikimedia.org/wikipedia/commons/c/cd/Accenture.svg",
  },
  {
    name: "Apple",
    logo: "https://upload.wikimedia.org/wikipedia/commons/f/fa/Apple_logo_black.svg",
  },
  {
    name: "Microsoft",
    logo: "https://upload.wikimedia.org/wikipedia/commons/9/96/Microsoft_logo_%282012%29.svg",
  },
  {
    name: "Google",
    logo: "https://upload.wikimedia.org/wikipedia/commons/2/2f/Google_2015_logo.svg",
  },
]
</script>

<template>
  <section class="container mx-auto">
    <div class="border-t border-b border-[#404040] py-16">
      <div
        class="max-w-3xl mx-auto px-4 flex justify-between items-center gap-8"
      >
        <img
          v-for="company in companies"
          :key="company.name"
          :src="company.logo"
          :alt="company.name"
          class="h-8 w-auto [filter:brightness(0)_invert(33%)] hover:[filter:brightness(1)_invert(0)] transition-[filter] duration-300"
        />
      </div>
    </div>
  </section>
</template>
