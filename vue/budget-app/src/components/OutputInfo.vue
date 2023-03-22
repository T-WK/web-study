<script setup lang="ts">
  import { defineProps } from 'vue';

  const props = defineProps<{title: string, value: number}>()
</script>

<template>
  <div>
    <p>{{ props.title }}</p>
    <span>{{ props.value }}</span>
  </div>
</template>