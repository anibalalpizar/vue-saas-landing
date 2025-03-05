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
  Legend,
  Filler
} from 'chart.js'

ChartJS.register(
  CategoryScale,
  LinearScale,
  PointElement,
  LineElement,
  Title,
  Tooltip,
  Legend,
  Filler
)

const chartData = {
  labels: ['AUG 21', 'AUG 22', 'AUG 23', 'AUG 24', 'AUG 25', 'AUG 26'],
  datasets: [
    {
      label: 'Dataset 1',
      data: [30, 45, 35, 50, 40, 35],
      borderColor: '#F59E0B',
      backgroundColor: 'rgba(245, 158, 11, 0.2)',
      fill: true,
      tension: 0.4,
      pointRadius: 0,
      borderWidth: 3
    },
    {
      label: 'Dataset 2',
      data: [20, 35, 25, 40, 30, 25],
      borderColor: '#6B7280',
      backgroundColor: 'rgba(107, 114, 128, 0.2)',
      fill: true,
      tension: 0.4,
      pointRadius: 0,
      borderWidth: 3
    }
  ]
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
        color: 'rgba(107, 114, 128, 0.1)'
      },
      ticks: {
        color: '#6B7280'
      }
    },
    y: {
      grid: {
        color: 'rgba(107, 114, 128, 0.1)'
      },
      ticks: {
        display: false
      }
    }
  }
}
</script>

<template>
  <div class="bg-[#2B2B2B] rounded-3xl p-6">
    <h3 class="text-lg font-semibold mb-4">Weekly plan</h3>
    <div class="h-[200px]">
      <Line :data="chartData" :options="chartOptions" />
    </div>
  </div>
</template>