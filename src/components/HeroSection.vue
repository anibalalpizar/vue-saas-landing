<script setup lang="ts">
import MonthlyPlan from "@/components/MonthlyPlan.vue"
import SpendingFrequency from "@/components/SpendingFrequency.vue"
import WeeklyPlan from "@/components/WeeklyPlan.vue"
</script>

<template>
  <main class="container mx-auto px-4 py-20">
    <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
      <div>
        <h2 class="text-6xl font-bold mb-6 leading-tight">
          SaaS Landing<br />Page Template
        </h2>
        <p class="text-gray-400 text-xl mb-8">
          This is a template Figma file, turned into code<br />using Anima.
          Learn more at AnimaApp.com
        </p>
        <button
          class="bg-[#E5B93E] hover:bg-[#D4A82D] text-black px-8 py-6 text-lg rounded-full transition-colors"
        >
          Get started
        </button>
      </div>

      <div class="bg-[#333333] rounded-[32px] p-8">
        <div class="grid grid-cols-2 gap-4">
          <MonthlyPlan class="col-span-1" />
          <SpendingFrequency class="col-span-1" />
          <WeeklyPlan class="col-span-2" />
        </div>
      </div>
    </div>
  </main>
</template>