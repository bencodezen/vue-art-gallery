<script>
export default {
  render(createElement) {
    return createElement(
      'svg',
      {
        viewBox: "0 0 100px 100px"
      },
      this.elements.map(element => 
        createElement(element.tag, {
          attrs: element.attrs
        })
      )
    )
  },
  props: {
    elements: {
      type: Array
    }
  }
}
</script>
