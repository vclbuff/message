<template>
  <div class="dm">
    <h1>
      Messages
    </h1>
    <div class="dm__inner">
      <OrganismsRoomList
        :items="dmList"
        class="dm__room"
      />
      <OrganismsRoomMessages
        class="dm__messages"
      />
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      dmList: [],
      message: []
    }
  },
  fetch () {
    this.dmList = [
      {
        username: 'usera',
        lastMessage: 'Hello'
      },
      {
        username: 'userb',
        lastMessage: 'Hello'
      },
      {
        username: 'userb',
        lastMessage: 'Hello'
      }
    ]
    this.messages = [
      {
        username: 'usera',
        postedAt: new Date().getTime(),
        message: 'Hello'
      },
      {
        username: 'usera',
        postedAt: new Date().getTime() + 1,
        message: 'World'
      },
      {
        username: 'userb',
        postedAt: new Date().getTime(),
        message: 'Hello'
      },
      {
        username: 'userc',
        postedAt: new Date().getTime(),
        message: 'Hello'
      }
    ]
  }
}
</script>

<style lang="scss">
.dm__inner {
  display: flex;
  min-height: calc(100vh - #{$headerHeight} - #{$footerHeight});
  border-top: 1px solid $cGray;
}

.dm__room {
  padding: $basePadding;
  border-right: 1px solid $cGray;
  width: 240px;
  flex-shrink: 0;
}

.dm__messages {
  padding: $basePadding;
  width: 100%;
}
</style>
