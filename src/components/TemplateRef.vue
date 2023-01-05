<template>
<div>TemplateRef
</div>
  <input type="text" ref="inputRef">
</template>

<script>
export default {
  name: "TemplateRef",
  mounted() {
    this.$refs.inputRef.focus();
  }
}
</script>

<style scoped>

</style>
