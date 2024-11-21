<script setup>
import { ref } from 'vue';

defineProps({
    tasks: Array,
})

const emit = defineEmits(['deleteTask'])

const deleteTask = (taskId) => {
    emit('deleteTask', taskId)
}
</script>

<template>
 <div>
    <h2>TaskList</h2>
    <ul>
        <li v-for="task in tasks" :key="task.id"> 
            {{ task.text }}
        <button @click="deleteTask(task.id)">Delete task</button>
        </li>
    </ul>
 </div>
</template>

<style>
</style>