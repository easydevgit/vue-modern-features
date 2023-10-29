<script setup lang="ts">
import DaisyUIModal from './components/DaisyUIModal.vue'
</script>

<template>
  <DaisyUIModal>
    <div>
      default slot
    </div>
    <template #body="{ short }">
      <p>Modal body first paragraph</p>
      <p v-if="!short">Modal body second paragraph</p>
    </template>
  </DaisyUIModal>
</template>
