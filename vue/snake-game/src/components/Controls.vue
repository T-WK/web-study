<template>
  <div class="controls">
    <font-awesome-icon icon="fa-solid fa-arrow-left-long" class="i" />
    <font-awesome-icon icon="fa-solid fa-arrow-up-long" class="i" />
    <font-awesome-icon icon="fa-solid fa-arrow-right-long" class="i" />
    <font-awesome-icon icon="fa-solid fa-arrow-down-long" class="i" />
  </div>
</template>

<style scoped>
  .controls {
    display: flex;
    justify-content: space-between;
  }
  .controls i {
    padding: 25px 0;
    text-align: center;
    font-size: 1.3rem;
    color: #b8c6dc;
    width: calc(100% / 4);
    cursor: pointer;
    border-right: 1px solid #171826;

  }
  @media screen and (max-width: 800px) {
    .controls {
        display: flex;
    }
    .controls .i {
        font-size: 1rem;
        padding: 15px 0;
    }
  }
</style>