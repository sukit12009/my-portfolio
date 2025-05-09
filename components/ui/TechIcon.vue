<template>
  <div class="flex flex-col items-center" :class="{ 'text-center': !small }">
    <div :class="iconContainerClass">
      <Icon :icon="icon" :class="iconClass" />
    </div>
    <span v-if="!small" class="mt-2 text-sm text-slate-400">{{ name }}</span>
  </div>
</template>

<script setup>
import { Icon } from '@iconify/vue';
import { computed } from 'vue';

const props = defineProps({
  name: {
    type: String,
    required: true
  },
  icon: {
    type: String,
    required: true
  },
  small: {
    type: Boolean,
    default: false
  }
});

const iconContainerClass = computed(() => {
  return props.small 
    ? 'w-full h-full flex items-center justify-center' 
    : 'w-16 h-16 bg-slate-800/80 rounded-xl flex items-center justify-center transform transition-transform hover:scale-110 duration-300';
});

const iconClass = computed(() => {
  return props.small ? 'w-6 h-6' : 'w-8 h-8';
});
</script>