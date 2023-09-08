<script setup lang="ts">
import { watchEffect } from 'vue'

// runtime declaration
// const props = defineProps({
//   msg: {
//     type: String,
//     required: false,
//     default: 'Hello'
//   }
// })

export interface Props {
  count?: number
}

// type declaration
const { count } = defineProps<Props>()

watchEffect(() => {
  console.log(count)
})

</script>

<template>
  <h1>{{ count }}</h1>
</template>
