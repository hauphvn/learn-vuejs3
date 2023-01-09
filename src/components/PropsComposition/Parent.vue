<template>
<div>Props composition api parent</div>
<ChildA first-name="hau" last-name="pham" @send-emit-key="onHandeSendEmitFromChild"/>
</template>

<script>
import ChildA from "@/components/PropsComposition/ChildA.vue";
import {computed} from "vue";

export default {
  name: "Parent",
  components: {ChildA},
  setup(){
    function onHandeSendEmitFromChild(data) {
      alert(data.msg)
    }
    return {
      onHandeSendEmitFromChild
    }
  }
}
</script>

<style scoped>

</style>
