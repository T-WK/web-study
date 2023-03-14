<script setup lang="ts">
  import GameDetails from './components/GameDetails.vue';
  import PlayBoard from './components/PlayBoard.vue'
  import Controls from './components/Controls.vue'
</script>

<template>
  <div class="wrapper">
    <GameDetails/>
    <PlayBoard/>
    <Controls/>
  </div>
</template>

<style scoped>
  .wrapper{ 
    width: 65vmin;
    height: 70vmin;
    display: flex;
    overflow: hidden;
    flex-direction: column;
    justify-content: center;
    background-color: #293447;
    border-radius: 5px;
    box-shadow: 0 20px 40px rgba(52, 87, 220, 0.2);
  }
  @media screen and (max-width: 800px) {
    .wrapper {
        width: 90vmin;
        height: 115vmin;
    }
  }
</style>