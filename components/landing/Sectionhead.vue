<script setup>
defineProps({
  align: {
    default: "center",
  },
});
</script>

<template>
  <div :class="['mt-16', align === 'center' && 'text-center']">
    <h1 class="text-4xl lg:text-5xl font-bold lg:tracking-tight">
      <slot name="title">Smith Creative</slot>
    </h1>
    <p class="text-lg mt-4 text-slate-600">
      <slot name="desc">Boutique Creative Group in Gardendale, AL</slot>
    </p>
  </div>
</template>
