<script setup lang="ts">
import ChildComponent from './components/ChildComponent.vue'
import { ref } from 'vue'

const greeting = ref('')
const farewell = ref('')

</script>

<template>
  <ChildComponent v-model:greeting="greeting" v-model:farewell="farewell" />

  <div>
    Greeting: {{ greeting }}
  </div>

  <div>
    Farewell: {{ farewell }}
  </div>
</template>
