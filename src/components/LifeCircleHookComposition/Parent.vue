<template>
  <div>Life circle hook composition</div>
</template>

<script>
import { onBeforeMount, onMounted, onBeforeUpdate, onUpdated, onBeforeUnmount, onUnmounted } from "vue";

export default {
  name: "Parent",
  setup() {
    onBeforeMount(() => {
      console.log('Life circle hook on before mount');
    });
    onMounted(() => {
      console.log('Life circle hook on mount');
    });
    onBeforeUpdate(() => {
      console.log('Life circle hook on before update');
    });
    onUpdated(() => {
      console.log('Life circle hook on update');
    });
    onBeforeUnmount(() => {
      console.log('Life circle hook on before unmount');
    });
    onUnmounted(() => {
      console.log('Life circle hook on unmount');
    });

  }
}
</script>

<style scoped>

</style>
