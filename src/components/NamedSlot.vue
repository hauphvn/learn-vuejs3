<template>
<div id="header">
  <slot>header default</slot>
</div>
  <div id="content">
    <slot name="content"></slot>
  </div>
  <div id="footer">
    <slot>footer default</slot>
  </div>
</template>

<script>
export default {
  name: "NamedSlot"
}
</script>

<style scoped>

</style>
