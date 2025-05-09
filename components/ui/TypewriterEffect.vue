<template>
  <span class="text-emerald-400">{{ displayText }}</span>
</template>

<script setup>
import { ref, onMounted, onBeforeUnmount } from "vue";

const props = defineProps({
  texts: {
    type: Array,
    required: true,
  },
  typingSpeed: {
    type: Number,
    default: 100,
  },
  erasingSpeed: {
    type: Number,
    default: 50,
  },
  delayAfterType: {
    type: Number,
    default: 2000,
  },
  delayAfterErase: {
    type: Number,
    default: 500,
  },
});

const displayText = ref("");
let currentTextIndex = 0;
let isTyping = true;
let charIndex = 0;
let timer = null;

const typeText = () => {
  const currentText = props.texts[currentTextIndex];

  if (isTyping) {
    if (charIndex < currentText.length) {
      displayText.value = currentText.substring(0, charIndex + 1);
      charIndex++;
      timer = setTimeout(typeText, props.typingSpeed);
    } else {
      isTyping = false;
      timer = setTimeout(typeText, props.delayAfterType);
    }
  } else {
    if (charIndex > 0) {
      displayText.value = currentText.substring(0, charIndex - 1);
      charIndex--;
      timer = setTimeout(typeText, props.erasingSpeed);
    } else {
      isTyping = true;
      currentTextIndex = (currentTextIndex + 1) % props.texts.length;
      timer = setTimeout(typeText, props.delayAfterErase);
    }
  }
};

onMounted(() => {
  timer = setTimeout(typeText, 500);
});

onBeforeUnmount(() => {
  clearTimeout(timer);
});
</script>
