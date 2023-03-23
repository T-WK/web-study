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


<style scoped>
  p{
      font-weight: 500;
      margin-bottom: 0.6em;
  }
  span{
      display: block;
      text-align: center;
      font-weight: 400;
      color: #e5e5e5;
  }
</style>