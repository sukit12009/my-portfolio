<template>
  <div class="flex flex-col items-center">
    <div
      class="w-16 h-16 flex items-center justify-center bg-slate-800 rounded-lg shadow-lg border border-slate-700/50 mb-2 transform transition-transform hover:scale-110 duration-300">
      <Icon :name="icon" class="w-10 h-10" />
    </div>
    <span class="text-sm text-slate-400">{{ name }}</span>
  </div>
</template>

<script setup>
defineProps({
  name: {
    type: String,
    required: true
  },
  icon: {
    type: String,
    required: true
  }
});
</script>