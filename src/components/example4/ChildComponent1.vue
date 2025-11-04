<template>
  <h3> Child 1 </h3>
  <div>
    <p>{{ sharedMessage }}</p>
  </div>

  <h3> Child 2 </h3>
  <div>
    <ChildComponent2 />
  </div>
</template>

<script>
import { inject } from 'vue'
import ChildComponent2 from '@/components/example4/ChildComponent2.vue'

export default {
  name: 'ChildComponent1',
  components: { ChildComponent2 },
  setup() {
    const sharedMessage = inject('sharedMessage')
    return { sharedMessage }
  },
}
</script>

<style scoped>
p {
  color: red;
}
</style>
