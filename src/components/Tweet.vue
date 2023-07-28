<script setup>
import User from "./User.vue";
import ProfileImage from "./ProfileImage.vue";
import Timestamp from "./Timestamp.vue";
import Message from "./Message.vue";
import Actions from "./Actions.vue";

const props = defineProps({
  user: Object,
  timestamp: String,
  message: String,
});
</script>

<template>
  <div class="tweet">
    <ProfileImage :image="user.image" />

    <div class="body">
      <div class="top">
        <User :userData="user" />
        <Timestamp :timestamp="timestamp" />
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
