<script setup>
import AddTask from './components/AddTask.vue';
import TaskList from './components/TaskList.vue';
import { ref } from 'vue';

const tasks = ref([
  { id: 1, text: 'Learn Vue.js' },
  { id: 2, text: 'Practice Composition API' },
  { id: 3, text: 'Build a cool app!' },
]);

const deleteTask = (taskId) => {
  tasks.value = tasks.value.filter((task) => task.id !== taskId); 
}

const addTask = (taskText) => {
  const newTask = {
    id: Date.now(), 
    text: taskText,
  };
  tasks.value.push(newTask);
};

</script>

<template>
  <div>
    <TaskList :tasks="tasks" @delete-task="deleteTask">

    </TaskList>
    <AddTask @add-task="addTask">

    </AddTask>
  </div>
</template>

<style scoped>

</style>
