<script lang="ts" setup>
  import SubContainer from './components/SubContainer.vue'
  import OutputContainer from './components/OutputContainer.vue'
  import List from './components/List.vue'

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

    <List>
    </List>
    
  </div>
</template>


<style scoped>
  .wrapper {
    width: 90%;
    font-size: 16px;
    max-width: 43.753m;
    margin: 1em auto;
  }
  .wrapper h3{
    color: #363d55;
    font-weight: 500;
    margin-bottom: 0.6em;
  }

  .container{
    width: 100%;
  }
  /* .container input{
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

  .container input:focus{
    border-color: #587ef4;
  } */
</style>