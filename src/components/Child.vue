
<!-- props -->
<!-- <template>
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
</script> -->

<!-- slot -->
<!-- <template>
  <div class="card">
    <h3>Child Component</h3>
    <slot></slot>
  </div>
</template>

<script setup>
import { onMounted } from 'vue'
import { useSlots } from 'vue'

const slots = useSlots()

onMounted(() => {
  console.log('[Child][Slot] slot default terdeteksi:', slots.default ? slots.default() : '—tidak ada—')
})
</script> -->

<!-- emit -->
<template>
  <div>
    <h3>Child Component</h3>
  </div>
</template>

<script setup>
import { onMounted } from 'vue'

const emit = defineEmits(['haloDariChild'])

onMounted(() => {
  console.log('[Child][Emit] akan emit event `haloDariChild`')
  emit('haloDariChild', 'Halo Parent, ini pesan otomatis dari Child!')
})
</script>
