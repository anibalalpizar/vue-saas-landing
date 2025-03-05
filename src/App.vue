<script setup lang="ts">
import { Button } from "@/components/ui/button"
import MonthlyPlan from "@/components/MonthlyPlan.vue"
import SpendingFrequency from "@/components/SpendingFrequency.vue"
import WeeklyPlan from "@/components/WeeklyPlan.vue"

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
  <div class="min-h-screen bg-[#2B2B2B] text-white">
    <!-- Navigation -->
    <nav class="container mx-auto px-4 py-6 flex justify-between items-center">
      <h1 class="text-2xl font-bold">Wallet</h1>
      <div class="flex gap-4 items-center">
        <Button variant="ghost" class="text-white">Sign up</Button>
        <Button class="bg-[#9747FF] hover:bg-[#8A3EFF]">Log in</Button>
      </div>
    </nav>

    <!-- Hero Section -->
    <main class="container mx-auto px-4 py-20">
      <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
        <div>
          <h2 class="text-6xl font-bold mb-6">SaaS Landing Page Template</h2>
          <p class="text-gray-400 text-xl mb-8">
            This is a template Figma file, turned into code using Anima. Learn
            more at AnimaApp.com
          </p>
          <Button
            class="bg-[#E5B93E] hover:bg-[#D4A82D] text-black px-8 py-6 text-lg"
          >
            Get started
          </Button>
        </div>

        <div class="grid grid-cols-2 gap-4">
          <MonthlyPlan class="col-span-1" />
          <SpendingFrequency class="col-span-1" />
          <WeeklyPlan class="col-span-2" />
        </div>
      </div>
    </main>

    <!-- Companies Section -->
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
            class="h-8 w-auto [filter:brightness(0)_invert(33%)]"
          />
        </div>
      </div>
    </section>
  </div>
</template>
