<template>
  <h1>Docker frontend + backend 🐳</h1>
  <p v-if="message">{{ message }}</p>
</template>

<script setup>
  import { ref, onMounted } from 'vue'

  const message = ref('')

  onMounted(async () => {
    const res = await fetch('http://localhost:3000/api/hello')
    const data = await res.json()
    message.value = data.message
  })
</script>

<style>
  body {
    font-family: sans-serif;
  }
</style>
