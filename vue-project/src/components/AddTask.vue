<script setup>
import { ref } from 'vue';

const newTaskText = ref('')

const emit = defineEmits(['addTask'])

const addTask = () => {
  if (newTaskText.value.trim()) {
    emit('add-task', newTaskText.value);
    newTaskText.value = ''; 
  }
};
</script>

<template>
 <div>
    <input v-model="newTaskText" type="text" placeholder="Enter a new task">
    <button @click="addTask">Add task</button>
 </div>
</template>

<style>
</style>