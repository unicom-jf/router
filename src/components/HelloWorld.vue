<script setup lang="ts">
import { shallowRef, ref } from 'vue';
import CompA from "./CompA.vue"
import CompB from "./CompB.vue"
const current = shallowRef(CompA)
const show = ref(true)
</script>

<template>
  <div>
    <div>
      <label><input type="radio" v-model="current" :value="CompA" />A</label>
    <label><input type="radio" v-model="current" :value="CompB" />B</label>
    <Transition>
      <KeepAlive>
        <component :is="current"></component>
      </KeepAlive>

      </Transition>
    <!-- <component :is="current"></component> -->
    <!-- <Transition>
      <component :is="current"></component>
    </Transition> -->

    </div>
    <div>
      <button @click=" show = !show">Toggle</button>
      <Transition>
        <p  v-if="show">hello</p>
      </Transition>
    </div>
  </div>
</template>

<style scoped>
h1 {
  font-weight: 500;
  font-size: 2.6rem;
  position: relative;
  top: -10px;
}

h3 {
  font-size: 1.2rem;
}

.greetings h1,
.greetings h3 {
  text-align: center;
}

@media (min-width: 1024px) {
  .greetings h1,
  .greetings h3 {
    text-align: left;
  }
}

.v-enter-active,
.v-leave-active {
  transition: opacity 0.5s ease;
}
.v-enter-from,
.v-leave-to {
  opacity: 0;
}
</style>
