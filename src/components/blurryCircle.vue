<template>
    <div
      class="absolute rounded-full pointer-events-none overflow-hidden"
      :style="{
        width: width,
        height: height,
        background: color,
        filter: 'blur(150px)',
        opacity: opacity,
        top: top,
        left: left,
        transform: 'translate(-50%, -50%)'
      }"
    ></div>
  </template>
  
  <script setup>
  const props = defineProps({
    width: {
      type: String,
      default: '400px'
    },
    height: {
      type: String,
      default: '400px'
    },
    color: {
      type: String,
      default: '#FFAC4C'
    },
    opacity: {
      type: Number,
      default: 0.4
    },
    top: {
      type: String,
      default: '50%'
    },
    left: {
      type: String,
      default: '50%'
    }
  })
  </script>
  
  <style scoped>
  /* Nothing else needed, all styles are inline for dynamic props */
  </style>
  