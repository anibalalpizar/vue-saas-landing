<script setup lang="ts">
import { Button } from "@/components/ui/button"
</script>

<template>
  <footer class="border-t border-[#404040] py-8">
    <div class="container mx-auto px-4">
      <div
        class="flex flex-col md:flex-row justify-between items-start md:items-center gap-6"
      >
        <div
          class="flex flex-col md:flex-row items-start md:items-center gap-6"
        >
          <span class="text-sm text-white">© Wallet 2022</span>
          <div class="flex gap-6 text-sm">
            <a href="#" class="text-white hover:text-gray-300 transition-colors"
              >Privacy policy</a
            >
            <a href="#" class="text-white hover:text-gray-300 transition-colors"
              >Cookies policy</a
            >
            <a href="#" class="text-white hover:text-gray-300 transition-colors"
              >Terms of use</a
            >
          </div>
        </div>
        <div
          class="flex flex-col md:flex-row items-start md:items-center gap-4"
        >
          <span class="text-sm text-[#E5B93E]"
            >Updates right to your inbox</span
          >
          <div class="flex gap-2 w-full md:w-auto">
            <input
              type="email"
              placeholder="Email Address"
              class="bg-[#333333] text-white text-sm px-4 py-2 rounded focus:outline-none focus:ring-1 focus:ring-[#E5B93E] w-full md:w-auto"
            />
            <Button class="bg-[#9747FF] hover:bg-[#8A3EFF] text-sm px-4"
              >CTA</Button
            >
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>
