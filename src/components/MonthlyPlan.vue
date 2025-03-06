<script setup lang="ts">
import { Doughnut } from "vue-chartjs"
import { Chart as ChartJS, ArcElement, Tooltip, Legend } from "chart.js"

ChartJS.register(ArcElement, Tooltip, Legend)

const chartData = {
  labels: ["Section 1", "Section 2", "Section 3", "Section 4"],
  datasets: [
    {
      data: [300, 200, 300, 200],
      backgroundColor: ["#3366FF", "#FFDF90", "#FF6250", "#009379"],
      borderWidth: 0,
    },
  ],
}

const chartOptions = {
  responsive: true,
  plugins: {
    legend: {
      display: false,
    },
  },
  cutout: "70%",
}
</script>

<template>
  <div class="bg-[#2B2B2B] rounded-2xl p-4">
    <h3 class="text-sm font-medium text-gray-400 mb-4">Monthly plan</h3>
    <div class="relative w-full aspect-square">
      <Doughnut :data="chartData" :options="chartOptions" />
    </div>
  </div>
</template>