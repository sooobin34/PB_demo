<template>
  <div>{{ fullName }}</div>
</template>

<script>
import { ref, computed, onMounted } from 'vue'

export default {
  name: "E02Reactive",

  setup() {
    const firstName = ref("Kyungsu")
    const lastName = ref("Lee")

    const fullName = computed(() => firstName.value + " " + lastName.value)

    onMounted(() => {
      setTimeout(() => {
        firstName.value = "KSL"
      }, 2000)
    })

    return { fullName }
  }
}
</script>
