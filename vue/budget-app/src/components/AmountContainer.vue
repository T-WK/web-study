<script lang="ts" setup>
  import { defineProps } from 'vue';

  const props = defineProps<{ title: string, errorMsg: string}>()
</script>

<template>
  <div>
    <h3>{{ props.title }}</h3>
    <p class="hide error">{{ props.errorMsg }}</p>
    <slot name="inputs"></slot>
  </div>
</template>

<style scoped>
  div {
    background: #fff;
    padding: 1.25em 0.9em;
    border-radius: 0.3em;
    box-shadow: 0 0.6em 1.2em rgba(28, 0, 80, 0.06);
  }

  .hide{
    display: none;
  }

  .error{
    color: #ff465a;
  }
</style>