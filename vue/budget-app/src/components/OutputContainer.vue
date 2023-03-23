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


<style scoped>
  .flex{
    display: flex;
    align-items: center;
  }

  .flex-space{
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .output-container{
    background-color: #587ef4;
    color: #fff;
    border-radius: 0.3em;
    box-shadow: 0 0.6em 1.2em rgba(28, 0, 80, 0.06);
    margin: 2em 0;
    padding: 1.2em;
  }
</style>