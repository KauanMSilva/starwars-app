<script setup lang="ts">
import { ref } from 'vue'

defineProps<{ msg: string }>()

const count = ref(0)
const mutiply = ref(0)
</script>

<template>
  <h1>{{ msg }}</h1>

  <input
    :value="mutiply"
    @input="event => mutiply = Number((event.target as HTMLInputElement).value)" type="number">
  <button @click="count++">Multiply</button>
  <div>
    <h1>Result</h1>
    <div class="row">
      <p>{{ mutiply }}</p>
      <p>X</p> 
      <p>{{ count }}</p>
      <p>=</p> 
      <p>{{ mutiply * count }}</p>
    </div>
  </div>
</template>

<style scoped>
.read-the-docs {
  color: #888;
}
.row{
  display: flex;
  gap: 10px;
}
</style>
