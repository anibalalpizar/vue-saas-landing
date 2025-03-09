<script setup lang="ts">
import Navigation from "@/components/Navigation.vue"
import HeroSection from "@/components/HeroSection.vue"
import CompaniesSection from "@/components/CompaniesSection.vue"
import DashboardPreview from "@/components/DashboardPreview.vue"
import FeaturesSection from "@/components/FeaturesSection.vue"
import TestimonialSection from "@/components/TestimonialSection.vue"
import CardsAnimation from "@/components/CardsAnimation.vue"
import Footer from "@/components/Footer.vue"
</script>

<template>
  <div class="min-h-screen bg-[#2B2B2B] text-white">
    <header role="banner">
      <Navigation />
    </header>

    <main role="main">
      <HeroSection />
      <CompaniesSection />
      <DashboardPreview />
      <FeaturesSection />
      <TestimonialSection />
      <CardsAnimation />
    </main>

    <footer role="contentinfo">
      <Footer />
    </footer>
  </div>
</template>
