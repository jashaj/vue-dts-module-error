<script setup lang="ts">
import { useCounterStore } from '@/lib'
import { storeToRefs } from 'pinia'

const counterStore = useCounterStore()
const { count } = storeToRefs(counterStore)

function buttonPressed() {
  counterStore.increment()
}
</script>

<template>
  <header>
    <h1>It works!</h1>
  </header>

  <main>
    <button @click="buttonPressed">Increment</button>
    <p>You have pressed the button {{ count }} times</p>
  </main>
</template>

<style scoped></style>
