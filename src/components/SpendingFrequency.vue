<script setup lang="ts">
import { Line } from 'vue-chartjs'
import {
  Chart as ChartJS,
  CategoryScale,
  LinearScale,
  PointElement,
  LineElement,
  Title,
  Tooltip,
  Legend
} from 'chart.js'

ChartJS.register(
  CategoryScale,
  LinearScale,
  PointElement,
  LineElement,
  Title,
  Tooltip,
  Legend
)

const chartData = {
  labels: ['MON', 'TUE', 'WED', 'THU', 'FRI', 'SAT'],
  datasets: [{
    label: 'Spending',
    data: [65, 85, 75, 90, 65, 75],
    borderColor: '#F59E0B',
    tension: 0.4,
    pointRadius: 0,
    borderWidth: 3
  }]
}

const chartOptions = {
  responsive: true,
  maintainAspectRatio: false,
  plugins: {
    legend: {
      display: false
    }
  },
  scales: {
    x: {
      grid: {
        display: false
      },
      ticks: {
        color: '#6B7280'
      }
    },
    y: {
      display: false
    }
  }
}
</script>

<template>
  <div class="bg-[#2C2C2C] rounded-3xl p-6">
    <h3 class="text-lg font-semibold mb-4">Spending frequency</h3>
    <div class="h-[150px]">
      <Line :data="chartData" :options="chartOptions" />
    </div>
  </div>
</template>