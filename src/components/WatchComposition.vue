<template>
<div>Watch user change Option</div>
  <input type="text" placeholder="enter value" v-model="user">
  <div>Old value: {{oldValue}}</div>
  <div>New value: {{newValue}}</div>
  <div>Watch user change Composition</div>
  <input type="text" placeholder="enter value" v-model="userComposition">
  <input type="text" placeholder="enter value 2" v-model="userComposition2">
  <div>Old value Composition: {{oldValueComposition}}</div>
  <div>New value Composition: {{newValueComposition}}</div>
  <hr>
  <div>Watch reactive</div>
  <input type="text" placeholder="watch reactive" v-model="usernameReactive">
  <input type="text" placeholder="watch reactive deeper" v-model="address.street">
</template>

<script>
import {ref, watch, reactive, toRefs} from "vue";

export default {
  name: "WatchComposition",
  data(){
    return {
      oldValue: '',
      newValue: '',
      user: ''
    }
  },
  watch: {
    user(newData, oldData) {
      this.oldValue = oldData;
      this.newValue = newData;
    }
  },
  setup(){
    const oldValueComposition = ref('');
    const newValueComposition = ref('');
    const userComposition = ref('');
    const userComposition2 = ref('');
    const userReactive = reactive({
      usernameReactive: '',
      emailReactive: '',
      address: {
        street: '',
        district: ''
      }
    });
    watch([userComposition, userComposition2],(newDatas, oldDatas)=>{
      console.log(newDatas[0], oldDatas[0])
      console.log(newDatas[1], oldDatas[1])
      // this.oldValueComposition = oldData;
      // this.newValueComposition = newData;
    });
    watch(() =>{
      return  {...userReactive}
    }, function (userNew, userOld){
      console.log('user old: ', userOld);
      console.log('user new: ', userNew);
    })
    // watch(() => {
    //   return userReactive.usernameReactive
    // },(usernameNew, usernameOld) => {
    //     console.log('user old: ', usernameOld);
    //     console.log('user new: ', usernameNew);
    // },);
    watch(() => {
    return  {...userReactive.address}
    },(streetOld,streetNew) => {
      console.log('street old: ', streetOld);
      console.log('street new: ', streetNew);
    },{
      deep: true
    })
    return {
      oldValueComposition, newValueComposition, userComposition, userComposition2, ...toRefs(userReactive)
    }
  }
}
</script>

<style scoped>

</style>
