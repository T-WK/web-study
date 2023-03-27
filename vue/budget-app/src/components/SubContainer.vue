<script setup lang="ts">
  import TotalAmountContainer from './TotalAmountContainer.vue'
  import UserAmountContainer from './UserAmountContainer.vue'
  
  import { ref, watch } from 'vue';
  import type { Ref } from 'vue';


  const words = ref([
    {title: 'Budget', errorMessage: 'Value cannot be empty or negative'},
    {title: 'Expenses', errorMessage: 'Value cannot be empty'}
  ])

  const tempAmount:Ref<number | string> = ref(0)

  watch(tempAmount, () => {
    console.log(tempAmount.value)
  })
</script>

<template>
  <div class="sub-container">
    <TotalAmountContainer 
    :title="words[0].title" 
    :errorMsg="words[0].errorMessage" 
    v-model="tempAmount"
    >
    </TotalAmountContainer>

    <UserAmountContainer 
    :title="words[1].title" 
    :errorMsg="words[1].errorMessage" 
    >
    </UserAmountContainer>
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