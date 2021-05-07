<template>
  <button @click="emitNativeEvent">Emit native event</button>
</template>

<script>
const mixin = {
  inheritAttrs: false,   // <---- this does not work
}

export default {
  name: 'MyComponent',
  //inheritAttrs: false,     // <---- this does work
  mixins: [ mixin ],
  methods: {
    emitNativeEvent() {
      this.$el.dispatchEvent(new Event('native-event'));
    }
  }
}
</script>
