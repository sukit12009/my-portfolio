<template>
  <component :is="tag" :href="href" :target="target" :type="type"
    class="inline-block px-6 py-3 rounded-md font-medium transition-all duration-300 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-offset-slate-900"
    :class="[
      primary ? 'bg-sky-500 hover:bg-sky-600 text-white focus:ring-sky-500' : '',
      secondary ? 'bg-emerald-500 hover:bg-emerald-600 text-white focus:ring-emerald-500' : '',
      outline ? 'bg-transparent border border-slate-600 hover:border-slate-400 text-slate-300 hover:text-slate-100 focus:ring-slate-500' : '',
      ghost ? 'bg-transparent hover:bg-slate-800 text-slate-300 hover:text-slate-100 focus:ring-slate-500' : '',
      disabled ? 'opacity-50 cursor-not-allowed' : '',
      className
    ]" :disabled="disabled">
    <slot></slot>
  </component>
</template>

<script setup>
defineProps({
  primary: Boolean,
  secondary: Boolean,
  outline: Boolean,
  ghost: Boolean,
  disabled: Boolean,
  tag: {
    type: String,
    default: 'button'
  },
  href: String,
  target: String,
  type: {
    type: String,
    default: 'button'
  },
  className: String
});
</script>