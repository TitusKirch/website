<template>
  <div
    :style="'width: ' + width + ';height: ' + height + ';'"
    class="flex items-center justify-center bg-gray-200 text-lg text-gray-500"
  >
    {{ width }} x {{ height }}
  </div>
</template>

<script setup lang="ts">
defineProps({
  width: {
    type: String,
    default: "100%",
  },
  height: {
    type: String,
    default: "150px",
  },
});
</script>
