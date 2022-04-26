<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <HelloWorld recipient="Nobody" msg="Hello Vue 3 + TypeScript + Vite" />
  <div>Recipient.Nobody === 'Nobody': {{ equalityCheck }}</div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import HelloWorld from './components/HelloWorld.vue'
import { Recipient } from './types';

export default defineComponent({
  components: { HelloWorld },
  setup() {
    const equalityCheck = Recipient.Nobody === 'Nobody';

    return { equalityCheck };
  }
})
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
