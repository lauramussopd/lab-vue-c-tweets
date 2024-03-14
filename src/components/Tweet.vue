<script setup>

import ProfileImage from './ProfileImage.vue';
import Timestamp from './Timestamp.vue';
import Message from './Message.vue';
import User from './User.vue';
import Actions from './Actions.vue';

defineProps({
  user: Object,
  timestamp: String,
  message: String
})

</script>

<template>
  <div class="tweet">
    <ProfileImage :imagePath="user.image" />

    <div class="body">
      <div class="top">
        <User :name="user.name" 
          :handle="user.handle"/>
        <Timestamp :time="timestamp" />
      </div>

      <Message :message="message" />

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
