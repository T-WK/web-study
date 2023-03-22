<script setup lang="ts">
  import { ref } from 'vue';

  import AmountContainer from './AmountContainer.vue'

  const words = ref([
    {title: 'Budget', errorMessage: 'Value cannot be empty or negative'},
    {title: 'Expenses', errorMessage: 'Value cannot be empty'}
  ])
</script>

<template>
  <div class="sub-container">
    <AmountContainer 
    :title="words[0].title" 
    :errorMsg="words[0].errorMessage" 
    class="total-amount-container"
    >
      <template v-slot:input>
        <input type="number" id="total-amount" placeholder="Enter Total Amount">
        <button class="submit" id="total-amount-button">Set Budget</button>
      </template>
    </AmountContainer>

    <AmountContainer 
    :title="words[0].title" 
    :errorMsg="words[0].errorMessage" 
    class="user-amount-container"
    >
      <template v-slot:input>
        <input type="text" class="product-title" id="product-title" placeholder="Enter Title Of Product">
        <input type="number" id="user-amount" placeholder="Enter Cost Of Product">
        <button class="submit" id="check-amount">Check Amount</button>
      </template>
    </AmountContainer>
  </div>
</template>