<template>
<div>child one</div>
  <ChildTwo/>
</template>

<script>
import ChildTwo from "@/components/ProvideInjectComposition/ChildTwo.vue";

export default {
  name: "ChildOne",
  components: { ChildTwo }
}
</script>

<style scoped>

</style>
