<template>
<!--  <h3 v-bind="$attrs">Greet component</h3>-->
  <h3>Greet component</h3>
  <div>
    <div>list props</div>
    {{name}}
    <br>
    {{username}}    <br>
    <p v-bind="$attrs">likes: </p>{{likes}}
    <p>email: {{email}}</p>
  </div>
</template>

<script>
// import { Animal } from "../models/Model";

export default {

  name: "GreetNameComponent",
  props: {
    name: String,
    username: String,
    heroName: String,
    likes: Number,
    email:{
      required: true,
      type: String,
      default: 'hauphvn@gmail.com'
    }

  },
  inheritAttrs: true
}
</script>

<style scoped>

</style>
