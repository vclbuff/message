<template>
  <footer class="footer">
    <small>
      {{ copyright }}
    </small>
  </footer>
</template>

<script>
export default {
  props: {
    copyright: {
      type: String,
      default: '© xxx',
      required: true
    }
  }
}
</script>

<style lang="scss" scoped>
</style>
