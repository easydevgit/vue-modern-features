<script setup lang="ts">
const greeting = defineModel<string>('greeting')
const farewell = defineModel<string>('farewell')

</script>

<template>
    <input v-model="greeting" />
    <input v-model="farewell" />
</template>