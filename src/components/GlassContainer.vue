<template>
    <div class="glass-tv-border m-2" :style="{ width: props.width, height: props.height,  borderRadius: props.rounded }">
        <!-- Slot for dynamic content -->
        <slot />
    </div>
</template>
  
<script setup>
const props = defineProps({
    width: {
        type: String,
        default: '100%'
    },
    height: {
        type: String,
        default: '100%'
    },
    rounded: {
        type: String,
        default: '0.5rem'
    }
})
</script>