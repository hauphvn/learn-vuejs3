<template>
<div>Tab a content</div>
  <div>count: {{countA}}</div>
  <button @click="increament">count</button>
</template>

<script>
export default {
  name: "TabA",
  data(){
    return {
      countA:1
    }
  },
  methods:{
    increament(){
      return this.countA += 1;
    }
  }
}
</script>

<style scoped>

</style>