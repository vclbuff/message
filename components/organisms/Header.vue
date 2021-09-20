<template>
  <header class="header">
    <div class="header__content">
      <h1 class="header__title">
        {{ title }}
      </h1>
      <nav>
        <ul class="header__list">
          <li
            v-for="item in items"
            :key="item.text"
            class="header__item"
          >
            <NuxtLink :to="item.to">
              {{ item.text }}
            </NuxtLink>
          </li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      default: 'Sample App',
      required: false
    },
    items: {
      type: Array,
      default: () => { return [] },
      required: true
    }
  }
}
</script>

<style lang="scss" scoped>
.header {
  background-color: $cBlack;
  color: white;
  height: $headerHeight;
}

.header__content {
  @include maxWidth();
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.header__list {
  list-style: none;
  font-size: 1.4rem;
}

.header__item {
  & > a {
    color: white;
    text-decoration: none;
    font-weight: bold;
  }
}
</style>
