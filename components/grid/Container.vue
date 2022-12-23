<template>
  <div
    class="grid grid-cols-1 gap-8"
    :class="{
      'md:grid-cols-2': cols === 2,
      'md:grid-cols-3': cols === 3,
      'grid-cols-2 md:grid-cols-4': cols === 4,
      'grid-cols-2 md:grid-cols-5': cols === 5,
      'grid-cols-2 md:grid-cols-4 lg:grid-cols-6': cols === 6,
      'grid-cols-2 md:grid-cols-4 lg:grid-cols-7': cols === 7,
      'grid-cols-2 md:grid-cols-4 lg:grid-cols-8': cols === 8,
      'grid-cols-2 md:grid-cols-4 lg:grid-cols-9': cols === 9,
      'grid-cols-2 md:grid-cols-4 lg:grid-cols-10': cols === 10,
      'grid-cols-2 md:grid-cols-4 lg:grid-cols-11': cols === 11,
      'grid-cols-2 md:grid-cols-4 lg:grid-cols-12': cols === 12,
    }"
  >
    <slot />
  </div>
</template>

<script setup lang="ts">
defineProps({
  cols: {
    type: Number,
    default: 2,
    validator: (value: number) => {
      return value >= 1 && value <= 12;
    },
  },
});
</script>
