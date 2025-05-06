<script setup lang="ts">
import { ref } from 'vue';
const count = ref(0)
</script>

<template>
  <div>
    <p>Component: A</p>
  <span> count: {{ count }}</span>
  <br/>
  <button @click="count++">+</button>

  </div>
</template>
<!-- 
<script setup>
import { ref } from 'vue'

const count = ref(0)
</script>

<template>
  <p>Current component: A</p>
  <span>count: {{ count }}</span>
  <button @click="count++">+</button>
</template> -->