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
    borderColor: '#EFCE7A',
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
        color: '#6B7280',
        font: {
          size: 10
        }
      }
    },
    y: {
      display: false
    }
  }
}
</script>

<template>
  <div class="bg-[#2B2B2B] rounded-2xl p-4">
    <h3 class="text-sm font-medium text-gray-400 mb-4">Spending frequency</h3>
    <div class="h-[120px]">
      <Line :data="chartData" :options="chartOptions" />
    </div>
  </div>
</template>