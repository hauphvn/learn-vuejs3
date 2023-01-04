<template>
  <div>List slot</div>
  <h3 v-for="user in users" :key="user.username">
    <slot :username="user.username" :email="user.email"></slot>
  </h3>
</template>

<script>
export default {
  name: 'ListSlot',
  data(){
    return {
      users: [
        {
          username: 'hau 1',
          email: 'hau1@gmail.com'
        },
        {
          username: 'hau 2',
          email: 'hau2@gmail.com'
        },
        {
          username: 'hau 3',
          email: 'hau3@gmail.com'
        }
      ]
    }
  }
}
</script>
<style scoped>

</style>
