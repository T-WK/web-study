<template>
  <div class="list">
    <h3>Expenses List</h3>
    <div class="list-container" id="list"></div>
  </div>
</template>


<style scoped>
  .list{
    background-color: #fff;
    padding: 1.8em 1.2em;
    box-shadow: 0 0.6em 1.2em rgba(28, 0, 80, 0.06);
    border-radius: 0.6em;
  }

  .sublist-content{
    width: 100%;
    border-left: 0.3em solid #587ef4;
    margin-bottom: 0.6em;
    padding: 0.5em 1em;
    display: grid;
    grid-template-columns: 3fr 2fr 1fr 1fr;
  }

  .product{
    font-weight: 500;
    color: #363d55;
  }

  .amount{
    color: #414a67;
    margin-left: 20%;
  }

  .icons-container{
    width: 5em;
    margin: 1.2em;
    align-items: center;
  }

  .product-title{
    margin-bottom: 1em;
  }

  .edit{
    margin-left: auto;
  }

  .edit, .delete{
    background: transparent;
    cursor: pointer;
    margin-right: 1.5em;
    border: none;
    color: #587ef4;
  }
</style>