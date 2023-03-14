<template>
  <div class="play-board"></div>
</template>

<style scoped>
  .play-board {
    height: 100%;
    width: 100%;
    display: grid;
    background: #212837;
    grid-template: repeat(30, 1fr) / repeat(30, 1fr);
  }
  .play-board .food {
      background: #ff003d;
  }
  .play-board .head {
      background: #60cdff;
  }

</style>