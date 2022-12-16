<template>
  <Space wrap>
      <Button @click="modal1 = true">Open Modal (default)</Button>
      <Button @click="modal2 = true">Open Modal (sticky)</Button>
      <Modal v-model="modal1" draggable scrollable :mask="false" title="Modal 1">
          <div>Modal 1</div>
          <div>Can be dragged off the screen</div>
      </Modal>
      <Modal v-model="modal2" draggable sticky scrollable :mask="false" title="Modal 2">
          <div>Modal 2</div>
          <div>Can’t be dragged out of the screen, it will be automatically adsorbed</div>
      </Modal>
  </Space>
</template>
<script>
  export default {
      data () {
          return {
              modal1: false,
              modal2: false
          }
      }
  }
</script>
