<template>
  <div>
    <h3>Child Component</h3>
    <p>Pesan dari Parent: {{ message }}</p>
  </div>
</template>

<script setup>
import { onMounted } from 'vue'

const props = defineProps({
  message: String
})

onMounted(() => {
  console.log('[Child][Props] menerima prop `message`:', props.message)
})
</script>
