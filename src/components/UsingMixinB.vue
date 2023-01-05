<template>
<div>
  <div>Using mixin B</div>
  <p @mouseover="incrementCount">Hover to increment count {{count}} count</p>
</div>
</template>

<script>
import counter from "@/mixins/counter";
export default {
  name: "UsingMixinB",
  mixins: [counter]
}
</script>

<style scoped>

</style>
