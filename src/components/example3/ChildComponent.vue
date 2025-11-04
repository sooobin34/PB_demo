<template>
  <div>
    <p>{{ message }}</p>
    <button @click="sendEvent">Send Event</button>
  </div>
</template>

<script>
export default {
  name: "ChildComponent",

  props: {
    message: {
      type: String,
      required: true
    }
  },

  setup(props, { emit }) {
    const sendEvent = () => {
      emit("custom-event", "Hello from child")
    }

    return {
      ...props,
      sendEvent
    }
  }
}
</script>
