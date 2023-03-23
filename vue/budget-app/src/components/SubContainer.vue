<script setup lang="ts">
  import AmountContainer from './AmountContainer.vue'
  
  import { ref } from 'vue';


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
    >
      <template v-slot:inputs>
        <input type="number" id="total-amount" placeholder="Enter Total Amount">
        <button class="submit" id="total-amount-button">Set Budget</button>
      </template>
    </AmountContainer>

    <AmountContainer 
    :title="words[0].title" 
    :errorMsg="words[0].errorMessage" 
    >
      <template v-slot:inputs>
        <input type="text" class="product-title" id="product-title" placeholder="Enter Title Of Product">
        <input type="number" id="user-amount" placeholder="Enter Cost Of Product">
        <button class="submit" id="check-amount">Check Amount</button>
      </template>
    </AmountContainer>
  </div>
</template>

<style scoped>
  .sub-container{
    width: 100%;
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 3em;
  }

  .submit{
    font-size: 1em;
    margin-top: 0.8em;
    background-color: #587ef4;
    border: none;
    outline: none;
    color: #fff;
    padding: 0.6em 1.2em;
    border-radius: 0.3em;
    cursor: pointer;
  }

  input{
    display: block;
    width: 100%;
    padding: 0.6em 0.3em;
    border: 1px solid #d0d0d0;
    border-radius: 0.3em;
    color: #414a67;
    outline: none;
    font-weight: 400;
    margin-bottom: 0.6em;
  }

  input:focus{
    border-color: #587ef4;
  }

  @media screen and (max-width: 600px) {
    .wrapper{
      font-size: 14px;
    }

    .sub-container{
      grid-template-columns: 1fr;
      gap: 1em;
    }
  }
</style>