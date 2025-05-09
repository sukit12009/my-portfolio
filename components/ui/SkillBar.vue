<template>
  <div>
    <div class="flex justify-between mb-1">
      <span class="text-slate-200">{{ name }}</span>
      <span class="text-slate-400">{{ percentage }}%</span>
    </div>
    <div class="h-2 bg-slate-700 rounded-full overflow-hidden">
      <div class="h-full rounded-full transition-all duration-1000" :class="[
        color === 'sky' ? 'bg-sky-500' : '',
        color === 'emerald' ? 'bg-emerald-500' : ''
      ]" :style="{ width: `${percentage}%` }"></div>
    </div>
  </div>
</template>

<script setup>
defineProps({
  name: {
    type: String,
    required: true
  },
  percentage: {
    type: Number,
    required: true
  },
  color: {
    type: String,
    default: 'sky',
    validator: (value) => ['sky', 'emerald'].includes(value)
  }
});
</script>