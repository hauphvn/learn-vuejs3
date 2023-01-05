<template>
<div>List posts</div>
<!--  <button @click="getPosts">Get posts</button>-->
 <div v-for="post in posts" :key="post.id">
   <div>UserId: {{post.userId}}</div>
   <div>Title: {{post.title}}</div>
 </div>
  <ModalMain :show= error @close="error = false"/>
</template>

<script>
import axios from "axios";
import ModalMain from "@/components/ModalMain.vue";
export default {
  name: "ListPosts",
  components:{
    ModalMain
  },
  data(){
    return {
      posts: [],
      error: false
    }
  },
  beforeUpdate() {
    console.log('before update')
  },
  updated() {
    console.log('updated')
  },
  mounted() {
    console.log('mounted')
  },
  beforeMount() {
    console.log('before mounted')
  },
  created() {
    this.getPosts();
      console.log('call api at created hook')
  },
  beforeCreate() {
    console.log('before created')
  },
  methods: {
    getPosts(){
      this.error = false;
      axios.get('https://jsonplaceholder.typicode.com/posts')
          .then((response) => {
           this.posts = response.data;
          })
          .catch((err) =>{
            console.log(err);
            this.error = true;
          })
    }
  }
}
</script>

<style scoped>

</style>
