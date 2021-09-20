<template>
  <ul class="room__list">
    <li
      v-for="item in items"
      :key="item.username"
      class="room__item"
    >
      {{ item.username }}
    </li>
  </ul>
</template>

<script>
export default {
  props: {
    items: {
      type: Array,
      requried: true,
      default: () => { return [] }
    }
  }
}
</script>

<style lang="scss" scoped>
.room__list {
  margin: 0;
}

.room__item {
  border-bottom: 1px solid $cGray;
  padding: $basePadding;
}
</style>
