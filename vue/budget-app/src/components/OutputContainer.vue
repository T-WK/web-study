<script setup lang="ts">
  import OutputInfo from './OutputInfo.vue';
  import { defineProps, ref } from 'vue';
  import type { Ref } from 'vue';

  const props = defineProps<{
    totalBudget: number, expenses: number, balance: number
  }>()

  const outputs:Ref<Array<string>> = ref(['Total Budget', 'Expenses', 'Balance'])
</script>

<template>
  <div class="output-container flex-space">
    <OutputInfo :title="outputs[0]" :value="props.totalBudget">
    </OutputInfo>

    <OutputInfo :title="outputs[1]" :value="props.expenses">
    </OutputInfo>

    <OutputInfo :title="outputs[2]" :value="props.balance">
    </OutputInfo>
  </div>
</template>