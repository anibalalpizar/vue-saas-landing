<script setup lang="ts">
import { Button } from "@/components/ui/button"
</script>

<template>
  <nav class="container mx-auto px-4 py-6 flex justify-between items-center">
    <h1 class="text-2xl font-bold">Wallet</h1>
    <div class="flex gap-4 items-center">
      <Button variant="ghost" class="text-white">Sign up</Button>
      <Button class="bg-[#9747FF] hover:bg-[#8A3EFF]">Log in</Button>
    </div>
  </nav>
</template>
