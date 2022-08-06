<template>
  <div className="tweet">
    <ProfileImage :image="user.image" />
    <div className="body">
      <div className="top">
        <User :userData="user" />
        <Timestamp :time="timestamp" />
      </div>
      <Message :message="message" />
      <Actions />
    </div>
    <i class="fas fa-ellipsis-h"></i>
  </div>
</template>

<script>
import ProfileImage from "./ProfileImage.vue";
import User from "./User.vue";
import Timestamp from "./Timestamp.vue";
import Message from "./Message.vue";
import Actions from "./Actions.vue";

export default {
  name: "Tweet",
  props: {
    tweet: Object,
  },
  data(){
    return{
      user: this.tweet.user,
      timestamp: this.tweet.timestamp,
      message: this.tweet.message,
    }
  },
  components: {
    ProfileImage,
    User,
    Timestamp,
    Message,
    Actions,
  },
};
</script>

<style scoped>
a {
  color: #42b983;
}
</style>
