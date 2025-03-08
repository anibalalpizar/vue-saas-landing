<script setup lang="ts">
import { Button } from "@/components/ui/button"
</script>

<template>
  <section class="container mx-auto py-20">
    <div class="max-w-5xl mx-auto px-4">
      <div
        class="flex flex-col-reverse lg:grid lg:grid-cols-2 gap-12 items-center"
      >
        <div class="text-center lg:text-left">
          <h2 class="text-5xl sm:text-6xl font-bold mb-6">
            Questions?<br />Let's talk
          </h2>
          <p class="text-gray-400 text-lg sm:text-xl mb-8">
            Contact us through our 24/7 live chat.<br />
            We're always happy to help!
          </p>
          <Button
            class="bg-[#E5B93E] hover:bg-[#D4A82D] text-black px-6 py-3 text-base rounded-full w-full sm:w-auto"
          >
            Get started
          </Button>
        </div>
        <div class="flex justify-center lg:justify-end">
          <img
            src="/gifts/cards.gif"
            alt="Cards Animation"
            class="w-full max-w-md lg:max-w-full rounded-lg shadow-lg bg-[#E1F6F4]"
          />
        </div>
      </div>
    </div>
  </section>
</template>
