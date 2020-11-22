<script>
export default {
  name: 'ModalJsx',

  props: {
    show: {
      type: Boolean,
      default: false
    }
  },

  render() {
    return this.show ? <div class="modal">
      <div class="content">{this.$slots.default}</div>
      <button onClick={this.clickCancelHandler}>Cancel</button>
      <button onClick={this.clickOkHandler}>Ok</button>
    </div> : null
  },

  methods: {
    clickCancelHandler() {
      console.log('Cancel click')
    },
    clickOkHandler() {
      console.log('Ok click')
    }
  }
}
</script>