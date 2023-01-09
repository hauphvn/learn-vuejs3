<template>
<div>TemplateRef
</div>
<!--  <div>Using option api</div>-->
<!--  <input type="text" ref="inputRef">-->
  <div>Using composition api</div>
  <input type="text" ref="inputRefCom">
</template>

<script>
import {ref, onMounted} from "vue";

export default {
  name: "TemplateRef",
  setup(){
    const inputRefCom = ref(null);
    onMounted(() => {
      inputRefCom.value.focus();
    });
    return {
      inputRefCom
    }
  },
  mounted() {
    // this.$refs.inputRef.focus();
  }
}
</script>

<style scoped>

</style>
