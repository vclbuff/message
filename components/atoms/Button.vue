<template>
  <button
    class="button"
    @click="submit"
  >
    <slot />
  </button>
</template>

<script>
export default {
  methods: {
    submit () {
      this.$emit('buttonClick')
    }
  }
}
</script>

<style lang="scss" scoped>
.button {
  background-color: $cAccent;
  color: white;
  padding: 8px 16px;
  border: 1px solid $cGray;
  border-radius: 4px;
}
</style>
