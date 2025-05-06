<script setup lang="ts">
import { ref } from 'vue';
const msg = ref('')
</script>

<template>
  <div>
    <p>Component: B</p>
  <span> message: {{ msg }}</span>
  <input v-model="msg"></input>

  </div>
</template>