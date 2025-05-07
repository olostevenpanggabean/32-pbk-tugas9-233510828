
<!-- props -->
<!-- <template>
  <div>
    <h2>Parent Component</h2>
    <Child :message="parentMessage" />
  </div>
</template>

<script setup>
import { onMounted, ref } from 'vue'
import Child from './components/Child.vue'

const parentMessage = ref('Halo dari Parent!')

onMounted(() => {
  console.log('[Parent][Props] mengirim prop `message`:', parentMessage.value)
})
</script> -->
 
<!-- slot -->
<template>
  <div>
    <h2>Parent Component</h2>
    <Child>
      <!-- ini konten slot -->
      <p>Ini konten dari Parent lewat slot.</p>
      <button @click="() => console.log('[Parent][Slot] tombol di slot diklik')">
        Klik Saya
      </button>
    </Child>
  </div>
</template>

<script setup>
import Child from './components/Child.vue'
</script>

