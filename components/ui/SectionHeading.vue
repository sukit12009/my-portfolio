<template>
  <div class="text-center">
    <h2
      class="text-3xl md:text-4xl font-bold text-slate-50 inline-block relative"
    >
      <slot></slot>
      <span
        class="absolute -bottom-2 left-0 w-full h-1 bg-gradient-to-r from-sky-400 to-emerald-400"
      >
      </span>
    </h2>
  </div>
</template>
