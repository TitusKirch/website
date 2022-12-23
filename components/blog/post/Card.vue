<template>
  <div
    class="flex overflow-hidden rounded-lg shadow-xl"
    :class="{
      'flex-col': type === 'vertical',
      'h-64 flex-row': type === 'horizontal',
    }"
  >
    <PlaceholderImage
      :height="{ vertical: '150px', horizontal: '100%' }[type]"
      :width="{ vertical: '100%', horizontal: '450px' }[type]"
      class="shrink-0"
    />
    <div class="flex flex-col gap-2 px-6 py-4">
      <span class="text-xl">Blog post</span>

      <p>
        Sint voluptate ea aliquip labore. Ipsum adipisicing consequat do esse ex
        ipsum magna officia nisi veniam non. Veniam amet excepteur in enim culpa
        aute in ut proident cupidatat. Nostrud amet minim eiusmod officia. Minim
        qui incididunt mollit pariatur nostrud culpa sint.
      </p>
    </div>
  </div>
</template>

<script setup lang="ts">
defineProps({
  type: {
    type: String,
    default: "vertical",
    validator: (value: string) => {
      return ["vertical", "horizontal"].includes(value);
    },
  },
});
</script>
