<template>
<div>
  <div>Using mixin component A</div>
  <button @click="incrementCount" >Click me to increment {{count}} count</button>
</div>
</template>

<script>
import counter from "@/mixins/counter";
export default {
  name: "UsingMixinA",
  data(){
    return {
      count: 100
    }
  },
  mixins: [counter]
}
</script>

<style scoped>

</style>
