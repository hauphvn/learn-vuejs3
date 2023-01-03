<template>
<div>This is popup</div>
  <div>data binding input: {{dataInput}}</div>
  <input type="text"  :value="propDataInput" @input="propDataInput = $event.target.value">
  <button @click="$emit('close',{message: 'okie'} )">Ok</button>
  <button @click="$emit('close')">Close</button>
</template>

<script>
export default {
  name: "Popup",
  data(){
    return{
      dataInput: ''
    }
  },
  props:{
    propDataInput: ''
  },
  emits:{
    close(message){
      return !!message ? message : ''
    }
  }
}
</script>

<style scoped>

</style>
