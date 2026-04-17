<script setup>
import { ref } from 'vue'

const count = ref(0)

function increment() {
  count.value++
}

function reset() {
  count.value = 0
}
</script>

<template>
  <div class="wrapper">
    <div class="card">
      <h2>Contador de Cliques</h2>
      <p>Você clicou <strong>{{ count }}</strong> vezes</p>
      <div class="buttons">
        <button @click="increment">Clique aqui</button>
        <button class="reset" @click="reset">Resetar</button>
      </div>
    </div>
  </div>
</template>

<style scoped>
.wrapper {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
}

.card {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 16px;
  font-family: sans-serif;
  background-color: #f9f9f9;
  padding: 40px 60px;
  border-radius: 16px;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1);
}

h2 {
  font-size: 1.5rem;
  color: #333;
}

p {
  font-size: 1.2rem;
  color: #555;
}

.buttons {
  display: flex;
  gap: 12px;
}

button {
  padding: 10px 28px;
  font-size: 1rem;
  background-color: #42b883;
  color: white;
  border: none;
  border-radius: 8px;
  cursor: pointer;
  transition: background-color 0.2s;
}

button:hover {
  background-color: #369a6e;
}

button.reset {
  background-color: #e74c3c;
}

button.reset:hover {
  background-color: #c0392b;
}
</style>
