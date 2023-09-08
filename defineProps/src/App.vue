<script setup lang="ts">
import { ref } from 'vue'
import ChildComponent from './components/ChildComponent.vue'
const count = ref(1)

</script>

<template>
  <ChildComponent :count="count" />
  <button @click="count++">Increase Count</button>
</template>


