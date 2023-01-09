<template>
  <div>Child props composition api</div>
  <div>Get full name from props: {{ getFullName }}</div>
  <button @click="sendEmit">Send emit</button>
</template>

<script>
import { computed } from 'vue';

export default {
  name: "ChildA",
  props: ['firstName', 'lastName'],
  emits:['sendEmitKey'],
  setup(props, context) {
    console.log('context: ', context)
    const getFullName = computed(() => {
      return `${props.firstName} | ${props.lastName}`;
    });
    function sendEmit() {
      context.emit('sendEmitKey', { msg: 'msg from child' })
    }
    return {
      getFullName,
      sendEmit
    }
  }
}
</script>

<style scoped>

</style>
