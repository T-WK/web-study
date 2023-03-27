<script setup>
  import { defineProps } from 'vue';
  import { computed } from 'vue'

  const props = defineProps(['title','errorMessage','modelValue'])

  const emit = defineEmits(['update:modelValue'])

  const value = computed({
    get() {
      return props.modelValue
    },
    set(value) {
      emit('update:modelValue', value)
    }
  })
</script>

<template>
  <div>
    <h3>{{ props.title }}</h3>
    <p class="hide error">{{ props.errorMsg }}</p>
    <input 
    :value="modelValue"
    @input="$emit('update:modelValue', $event.target.value)"
    type="number" placeholder="Enter Total Amount">
    <button class="submit" id="total-amount-button">Set Budget</button>
  </div>
</template>

<style scoped>
  div {
    background: #fff;
    padding: 1.25em 0.9em;
    border-radius: 0.3em;
    box-shadow: 0 0.6em 1.2em rgba(28, 0, 80, 0.06);
  }

  .hide{
    display: none;
  }

  .error{
    color: #ff465a;
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
</style>