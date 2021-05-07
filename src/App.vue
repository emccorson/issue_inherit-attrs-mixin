<template>
  <MyComponent @native-event="handleNativeEvent" />
</template>

<script>
import MyComponent from './MyComponent.vue'

export default {
  name: 'App',
  components: {
    MyComponent
  },
  methods: {
    handleNativeEvent() {
      alert('There was a native event');
    }
  }
}
</script>
