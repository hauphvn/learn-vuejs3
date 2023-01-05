<template>
<button @click="tabName = 'TabA'">TabA</button>
<button @click="tabName = 'TabB'">TabB</button>
<keep-alive>
<component :is="tabName"/>
</keep-alive>
</template>

<script>
import TabA from "./TabA.vue";
import TabB from "./TabB.vue";
export default {
  name: "TabIndex",
  components:{
    TabA, TabB
  },
  data(){
    return {
      tabName: 'TabA'
    }
  }
}
</script>

<style scoped>

</style>