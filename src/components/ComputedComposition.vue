<template>
<div>Option computed</div>
  <input type="text" placeholder="username" v-model="oUsername">
  <input type="text" placeholder="email" v-model="oEmail">
  <div>{{getUserOption}}</div>
  <div>Composition computed</div>
  <input type="text" placeholder="username" v-model="cUsername">
  <input type="text" placeholder="email" v-model="cEmail">
  <div>{{getUserComposition}}</div>
</template>

<script>
import {reactive, toRefs, computed} from "vue";

export default {
  name: "ComputedComposition",
  data() {
    return {
      oUsername: '',
      oEmail: ''
    }
  },
  computed:{
    getUserOption(){
      return `${this.oUsername} | ${this.oEmail}`
    }
  },
  setup(){
    const user = reactive({
      cUsername: '',
      cEmail: ''
    });

    const getUserComposition = computed(function(){
      return `${user.cUsername} | ${user.cEmail}`
    });
    return ({
      ...toRefs(user),
      getUserComposition
    });
  }
}
</script>

<style scoped>

</style>
