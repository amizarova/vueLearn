<script setup>
import { ref } from 'vue';
  const count = ref(1);
  const increment = () => {
    count.value++
  }
</script>

<template>
  <div class="container">
    <strong>
      {{ count }}
     </strong>
    <button @click="increment">
      Нажми, чтобы увеличить это число
    </button>

  </div>
</template>

<style scoped>
button {
  border: 2px solid black;
  border-radius: 5px;
  font-size: 16px;
  padding: 5px;
  background-color: rgb(197, 197, 197);
  cursor: pointer;
}
.container {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 10px;
  font-size: 20px;
  flex-direction: column;
}
</style>
