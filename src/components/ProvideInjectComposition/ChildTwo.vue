<template>
<div>Child two</div>
<div>data from parent: {{dataFromParent}}</div>
<div>data from parent dataParentReActive: {{JSON.stringify(dataParentReActive)}}</div>

</template>

<script>
import {inject} from "vue";

export default {
  name: "ChildTwo",
  setup(){
    const dataFromParent = inject('dataParent', 'Data default if undefined');
    const dataParentReActive = inject('dataParentReActive', 'default')
    return ({
      dataFromParent, dataParentReActive
    })
  }
}
</script>

<style scoped>

</style>
