<template>
  <div class="style-component-1">Style component other</div>
  <h4>style component other h4</h4>
  <div>Beside is slot</div>
  <slot></slot>
</template>

<script>
export default {
  name: "StyleOtherComponent"
}
</script>

<style scoped>
.style-component-1{
  color: blue;
}
h4{
  background-color: blue;
  color: white;
}
</style>
