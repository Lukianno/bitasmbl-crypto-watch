<template>
  <main class="min-h-screen bg-gray-900 text-white p-6">
    <h1 class="text-3xl font-bold mb-6">📊 Crypto Dashboard</h1>

    <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-4">
      <div
        v-for="ticker in cryptoTickers"
        :key="ticker.symbol"
        class="bg-gray-800 p-4 rounded-xl shadow border border-gray-700"
      >
        <h2 class="text-xl font-semibold">{{ ticker.name }}</h2>
        <p class="text-sm text-gray-400">{{ ticker.symbol }}</p>
        <p class="text-lg mt-2">${{ ticker.price.toFixed(2) }}</p>
      </div>
    </div>
  </main>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const cryptoTickers = ref([
  { name: 'Bitcoin', symbol: 'BTC', price: 30250.45 },
  { name: 'Ethereum', symbol: 'ETH', price: 1875.99 },
  { name: 'Solana', symbol: 'SOL', price: 42.30 },
  { name: 'Cardano', symbol: 'ADA', price: 0.33 },
]);
</script>
