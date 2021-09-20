<template>
  <form
    action=""
    onSubmit="return false"
    class="form"
  >
    <textarea
      v-model="message"
      rows="1"
      class="form__textarea"
    />
    <AtomsButton
      class="form__button"
      @buttonClick="post"
    >
      送信する
    </AtomsButton>
  </form>
</template>

<script>
export default {
  data () {
    return {
      message: ''
    }
  },
  methods: {
    post () {
    }
  }
}
</script>

<style lang="scss" scoped>
.form {
  display: flex;
}

.form__textarea {
  resize: none;
  width: 100%;
}

.form__button {
  flex-shrink: 0;
}
</style>
