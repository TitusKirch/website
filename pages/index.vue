<template>
  <div class="h-full w-full bg-gray-50 p-4">
    <GridContainer :cols="1">
      <GridContainer :cols="3">
        <BlogPostCard />
        <BlogPostCard />
        <BlogPostCard />
      </GridContainer>

      <GridContainer :cols="1">
        <BlogPostCard type="horizontal" />
        <BlogPostCard type="horizontal" />
        <BlogPostCard type="horizontal" />
      </GridContainer>
    </GridContainer>
  </div>
</template>

<script setup lang="ts"></script>
