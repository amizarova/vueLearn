<script setup>
import { ref } from 'vue';

const users = ref([
  {id: 1, name: 'Эмиль', age: '21'},
  {id: 2, name: 'Ева', age: '25'},
  {id: 3, name: 'Олег', age: '50'},
])
</script>

<template>
  <div>
    <ul>
      <li 
      v-for="user in users" 
      :key="user.id"
      v-show="user.age > 21"
      >
        {{ user.name}} 
        <sup v-if="user.name !== 'Олег'">{{ user.age }}</sup>
        <sup v-else> в возрасте...</sup>
      </li>
    </ul>
  </div>
</template>

<style scoped>

</style>
