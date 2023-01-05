<template>
  <div>Tab b content</div>
  <div>count: {{countB}}</div>
  <button @click="increament">count</button>
</template>

<script>
export default {
  name: "TabB",
  data(){
    return {
      countB: 1
    }
  },
  methods:{
    increament(){
      this.countB += 1;
    }
  }
}
</script>

<style scoped>

</style>