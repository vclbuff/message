<template>
  <div class="message">
    <ul class="message__list">
      <li
        v-for="item in items"
        :key="item.postedAt"
        class="message__item"
      >
        {{ item.username }}
        {{ item.postedAt }}
        {{ item.message }}
      </li>
    </ul>
    <AtomsPostMessage
      class="message__post"
    />
  </div>
</template>

<script>
export default {
  props: {
    messages: {
      type: Array,
      required: false,
      default: () => { return [] }
    }
  }
}
</script>

<style lang="scss" scoped>
.message {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}
.message__list {
  list-style: none;
}
</style>
