<template>
<div>Hero name: {{heroName}}</div>
<div>Username: {{username}}</div>
<div>Email: {{email}}</div>
  <br>
  <input type="text" v-model="heroName" placeholder="hero name">
  <input type="text" v-model="username" placeholder="username">
  <input type="text" v-model="email" placeholder="email">
</template>

<script>
import {ref, reactive, toRefs} from "vue";

export default {
  name: "CompositionApiVModel",
  setup(){
    const heroName = ref('');
    const user = reactive({
      username: '',
      email: ''
    });
    return {
      heroName,
      ...toRefs(user)
    }
  }
}
</script>

<style scoped>

</style>
