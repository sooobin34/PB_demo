<template>
  <div>
    <p>{{ sharedMessage }}</p>
  </div>
</template>

<script>
import { inject } from 'vue'

export default {
  name: 'ChildComponent2',
  setup() {
    const sharedMessage = inject('sharedMessage')
    return { sharedMessage }
  },
}
</script>

<style scoped>
p {
  font-size: 1.5rem;
}
</style>
