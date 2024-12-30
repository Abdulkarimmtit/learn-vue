<script lang="ts">
import { defineComponent, ref } from 'vue'

export default defineComponent({
  setup() {
    const count = ref(0) // Declarando uma variável reativa

    const increment = () => {
      count.value++ // Atualizando o valor reativo
    }

    return {
      count,
      increment, // Tornando acessível no template
    }
  },
})
</script>

<template>
  <div>
    <p>Count: {{ count }}</p>
    <button @click="increment">Increment</button>
  </div>
</template>
