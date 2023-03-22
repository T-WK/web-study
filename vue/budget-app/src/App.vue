<script lang="ts" setup>
  import SubContainer from './components/SubContainer.vue'
  import OutputContainer from './components/OutputContainer.vue'
  import { ref } from 'vue'
  import type { Ref } from 'vue'


  const totalBudget:Ref<number> = ref(0)
  const expenses:Ref<number> = ref(0)
  const balance:Ref<number> = ref(0)
</script>


<template>
  <div class="wrapper">
    <div class="container">
      
      <SubContainer>
      </SubContainer>

      <OutputContainer
      :totalBudget="totalBudget"
      :expenses="expenses"
      :balance="balance"
      >
      </OutputContainer>

    </div>

    <div class="list">
      <h3>Expenses List</h3>
      <div class="list-container" id="list"></div>
    </div>
  </div>
</template>