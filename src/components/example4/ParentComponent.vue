<template>
  <div>
    <ChildComponent1 />
  </div>
</template>

<script>
import { provide } from 'vue'
import ChildComponent1 from '@/components/example4/ChildComponent1.vue'

export default {
  name: 'E06ParentComponent',
  components: { ChildComponent1 },
  setup() {
    // Vue2의 provide() 반환값과 동일한 역할
    provide('sharedMessage', 'Hello from provide')
    return {}
  },
}
</script>
