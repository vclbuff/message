<template>
  <ul class="room__list">
    <li
      v-for="item in items"
      :key="item.username"
      class="room__item"
    >
      <p class="user__name">
        {{ item.username }}
      </p>
      <p class="user__message">
        {{ item.lastMessage }}
      </p>
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

.user__name {
  font-size: 1.4rem;
  font-weight: bold;
  margin: 0;
}

.user__message {
  color: gray;
  margin: 0;
  text-align: right;
}
</style>
