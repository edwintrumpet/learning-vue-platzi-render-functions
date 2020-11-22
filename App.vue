<template>
  <div id="app">
    <button @click.prevent="toggleHandler">Toggle Modal</button>
    <modal-create-element :show="show" message="Hello world!"></modal-create-element>
  </div>
</template>

<script>
import ModalCreateElement from './ModalCreateElement.vue'

export default {
  name: "App",
  components: {
    ModalCreateElement
  },
  data() {
    return {
      show: false
    }
  },
  methods: {
    toggleHandler() {
      this.show = !this.show
    }
  }
}
</script>
