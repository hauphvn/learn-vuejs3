<template>
  <teleport to="#modal-root">
    <div v-show="show" class="modal-wrapper">
      <div class="modal">
        <div class="modal-header">header</div>
        <div class="modal-content">content</div>
        <div class="modal-footer">
          <button @click="$emit('close')">Close</button>
        </div>
      </div>
    </div>
  </teleport>
</template>

<script>
export default {
  name: "ModalMain",
  props: {
    show: false
  },
  methods: {
  }
}
</script>

<style scoped>
.modal-wrapper{
  position: fixed;
  top: 0;
  left: 0;
  //right: 0;
  //bottom: 0;
  display: flex;
  justify-content: center;
  text-align: center;
  min-width: 100%;
  min-height: 100%;
  background-color: rgba(0,0,0,0.4);
  z-index: 9999;
}
.modal-wrapper > .modal{
  background-color: white;
  border: 1px solid orange;
  position: absolute;
  min-width: 300px;
  min-height: 200px;
  top: 100px;
}
</style>
