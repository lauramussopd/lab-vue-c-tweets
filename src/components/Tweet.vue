<script setup>

import ProfileImage from './ProfileImage.vue';
import Timestamp from './Timestamp.vue';
import Message from './Message.vue';
import User from './User.vue';
import Actions from './Actions.vue';

defineProps({
  content: Object
})

</script>

<template>
  <div class="tweet">
    <ProfileImage :image="content.user.image" />

    <div class="body">
      <div class="top">
        <User :userData="content.user" />
        <Timestamp :time="content.timestamp" />
      </div>

      <Message :message="content.message" />

      <Actions />

    </div>

    <i class="fas fa-ellipsis-h"></i>
  </div>
</template>

<style scoped>
a {
  color: #42b983;
}
</style>
