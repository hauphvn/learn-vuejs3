<template>
<div>parent</div>
  <button @click="changeData">change data</button>
  <ChildOne/>
</template>

<script>
import ChildOne from "@/components/ProvideInjectComposition/ChildOne.vue";
import {provide, reactive, ref, toRefs} from "vue";

export default {
  name: "Parent",
  components: { ChildOne },
  setup(){
    const dataParent = ref('hauphvn');
    const dataParentReActive = reactive({
      username: 'hauhpvn',
      email: 'hauphbn email'
    })
    function changeData() {
      dataParent.value = 'hauphvn updated';
    }
    provide('dataParent', dataParent);
    provide('dataParentReActive', dataParentReActive);
    return {
      changeData
    }
  }
}
</script>

<style scoped>

</style>
