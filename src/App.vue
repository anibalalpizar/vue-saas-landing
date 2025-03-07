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
          <h2 class="text-6xl font-bold mb-6 leading-tight">
            SaaS Landing<br />Page Template
          </h2>
          <p class="text-gray-400 text-xl mb-8">
            This is a template Figma file, turned into code<br />using Anima.
            Learn more at AnimaApp.com
          </p>
          <Button
            class="bg-[#E5B93E] hover:bg-[#D4A82D] text-black px-8 py-6 text-lg rounded-full"
          >
            Get started
          </Button>
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

    <!-- Dashboard Preview Section -->
    <section class="container mx-auto py-20">
      <div class="max-w-5xl mx-auto px-4 bg-[#FDF5DF]">
        <img
          src="/images/dashboard-preview.png"
          alt="Dashboard Preview"
          class="w-full rounded-3xl shadow-xl"
        />
      </div>
    </section>

    <!-- Features Section -->
    <section class="container mx-auto py-20">
      <div class="grid grid-cols-1 md:grid-cols-3 gap-8 max-w-5xl mx-auto px-4">
        <!-- Customizable card -->
        <div class="text-center">
          <div
            class="bg-[#333333] w-16 h-16 rounded-xl flex items-center justify-center mx-auto mb-6"
          >
            <svg
              width="32"
              height="32"
              viewBox="0 0 32 32"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M26.6667 8H5.33333C4.59695 8 4 8.59695 4 9.33333V22.6667C4 23.403 4.59695 24 5.33333 24H26.6667C27.403 24 28 23.403 28 22.6667V9.33333C28 8.59695 27.403 8 26.6667 8Z"
                stroke="#3B82F6"
                stroke-width="2"
                stroke-linecap="round"
                stroke-linejoin="round"
              />
              <path
                d="M4 13.3333H28"
                stroke="#3B82F6"
                stroke-width="2"
                stroke-linecap="round"
                stroke-linejoin="round"
              />
            </svg>
          </div>
          <h3 class="text-xl font-semibold mb-4">Customizable card</h3>
          <p class="text-gray-400">
            Custom your own card for your exact incomes and expenses needs.
          </p>
        </div>

        <!-- No payment fee -->
        <div class="text-center">
          <div
            class="bg-[#333333] w-16 h-16 rounded-xl flex items-center justify-center mx-auto mb-6"
          >
            <svg
              width="32"
              height="32"
              viewBox="0 0 32 32"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <circle cx="16" cy="16" r="12" fill="#9747FF" />
              <path
                d="M16 10.6667V21.3334"
                stroke="white"
                stroke-width="2"
                stroke-linecap="round"
                stroke-linejoin="round"
              />
              <path
                d="M10.6667 16H21.3334"
                stroke="white"
                stroke-width="2"
                stroke-linecap="round"
                stroke-linejoin="round"
              />
            </svg>
          </div>
          <h3 class="text-xl font-semibold mb-4">No payment fee</h3>
          <p class="text-gray-400">
            Transfer your payment all over the world with no payment fee.
          </p>
        </div>

        <!-- All in one place -->
        <div class="text-center">
          <div
            class="bg-[#333333] w-16 h-16 rounded-xl flex items-center justify-center mx-auto mb-6"
          >
            <svg
              width="32"
              height="32"
              viewBox="0 0 32 32"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M25.3333 5.33334H6.66667C5.93029 5.33334 5.33334 5.93029 5.33334 6.66667V25.3333C5.33334 26.0697 5.93029 26.6667 6.66667 26.6667H25.3333C26.0697 26.6667 26.6667 26.0697 26.6667 25.3333V6.66667C26.6667 5.93029 26.0697 5.33334 25.3333 5.33334Z"
                fill="#E5B93E"
              />
              <path
                d="M12 26.6667V12"
                stroke="white"
                stroke-width="2"
                stroke-linecap="round"
                stroke-linejoin="round"
              />
              <path
                d="M5.33334 12H26.6667"
                stroke="white"
                stroke-width="2"
                stroke-linecap="round"
                stroke-linejoin="round"
              />
            </svg>
          </div>
          <h3 class="text-xl font-semibold mb-4">All in one place</h3>
          <p class="text-gray-400">
            The right place to keep your credit and debit cards, boarding passes
            & more.
          </p>
        </div>
      </div>
    </section>

    <!-- Testimonial Section -->
    <section class="container mx-auto py-20">
      <div class="max-w-5xl mx-auto px-4">
        <div class="bg-[#BFAFF2] rounded-3xl p-12">
          <div class="max-w-3xl">
            <p class="text-2xl mb-8 leading-relaxed">
              "Wallet is a great product! All of my most important information
              is there - credit cards, transit cards, boarding passes, tickets,
              and more. And I don't need to worry because it's all in one place!
              thanks!"
            </p>
            <div class="flex items-center gap-4">
              <img
                src="/images/profile.png"
                alt="Johnny Owens"
                class="w-12 h-12 rounded-full"
              />
              <div>
                <h4 class="font-semibold">Johnny Owens</h4>
                <div class="flex gap-1">
                  <svg
                    v-for="i in 5"
                    :key="i"
                    width="16"
                    height="16"
                    viewBox="0 0 16 16"
                    fill="none"
                    xmlns="http://www.w3.org/2000/svg"
                  >
                    <path
                      d="M8 1L10.163 5.279L15 6.017L11.5 9.389L12.326 14L8 11.838L3.674 14L4.5 9.389L1 6.017L5.837 5.279L8 1Z"
                      fill="currentColor"
                    />
                  </svg>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Cards Animation Section -->
    <section class="container mx-auto py-20">
      <div class="max-w-5xl mx-auto px-4">
        <div class="flex flex-col-reverse lg:grid lg:grid-cols-2 gap-12 items-center">
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

    <!-- Footer -->
    <footer class="border-t border-[#404040] py-8">
      <div class="container mx-auto px-4">
        <div class="flex flex-col md:flex-row justify-between items-start md:items-center gap-6">
          <div class="flex flex-col md:flex-row items-start md:items-center gap-6">
            <span class="text-sm text-white">© Wallet 2022</span>
            <div class="flex gap-6 text-sm">
              <a href="#" class="text-white hover:text-gray-300 transition-colors">Privacy policy</a>
              <a href="#" class="text-white hover:text-gray-300 transition-colors">Cookies policy</a>
              <a href="#" class="text-white hover:text-gray-300 transition-colors">Terms of use</a>
            </div>
          </div>
          <div class="flex flex-col md:flex-row items-start md:items-center gap-4">
            <span class="text-sm text-[#E5B93E]">Updates right to your inbox</span>
            <div class="flex gap-2 w-full md:w-auto">
              <input
                type="email"
                placeholder="Email Address"
                class="bg-[#333333] text-white text-sm px-4 py-2 rounded focus:outline-none focus:ring-1 focus:ring-[#E5B93E] w-full md:w-auto"
              />
              <Button class="bg-[#9747FF] hover:bg-[#8A3EFF] text-sm px-4">CTA</Button>
            </div>
          </div>
        </div>
      </div>
    </footer>
  </div>
</template>