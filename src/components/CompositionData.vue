<template>
  <div>Composition data</div>
  <div>Option data old {{ optionData }}</div>
  <div>Composition data: {{ compositionData }}</div>
  <div>Composition data without ref will no updated: {{compositionDataWithOutRef}}</div>
  <div>Composition data object: {{ compositionDataObject.username }} | {{ compositionDataObject.email }}</div>
<div>Username from object: {{usernameFromObject}}</div>
  <button @click="updateUser">Update with method in composition api</button>
</template>

<script>
import { reactive, ref, toRefs} from "vue";

export default {
  name: "CompositionData",
  setup() {
    const compositionData = ref('compositionData');
    let compositionDataWithOutRef = 'compositionDataWithOutRef'
    const compositionDataObject = reactive({
      username: 'hauphvn',
      email: 'hauphvn@gmail.com'
    });
    function updateUser () {
      compositionDataObject.username = 'update username via method';
      compositionDataObject.email = 'update email via method';
    }
    setTimeout(() => {
      compositionDataWithOutRef = 'compositionDataWithOutRef update';
      compositionData.value = 'composition data updated';
      compositionDataObject.username ='hauphvn updated'
    },2000)
    return {
      compositionData,
      compositionDataObject,
      compositionDataWithOutRef,
      usernameFromObject:(compositionDataObject.username),
      updateUser
    }
    // return toRefs(compositionDataObject);
  },
  data() {
    return {
      optionData: 'Option data'
    }
  }
}
</script>

<style scoped>

</style>
