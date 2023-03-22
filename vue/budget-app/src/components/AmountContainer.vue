<script lang="ts" setup>
  import { defineProps } from 'vue';
  const props = defineProps<{ title: string, errorMsg: string}>()
</script>

<template>
  <div>
    <h3>{{ props.title }}</h3>
    <p class="hide error">{{ props.errorMsg }}</p>
    <slot name="input"></slot>
  </div>
</template>