<script setup>
import { ref } from 'vue'

const count = ref(0)

function increment() {
  count.value++
}
</script>

<template>
  <div>
    <h2>Contador de Cliques</h2>
    <p>Você clicou <strong>{{ count }}</strong> vezes</p>
    <button @click="increment">Clique aqui</button>
  </div>
</template>
