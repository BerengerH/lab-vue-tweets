<template>
  <div className="actions">
    <!-- Font Awesome icons -->
    <i class="far fa-comment pointer"></i>
    <i @click="retweet" class="fas fa-retweet pointer" :class="{'retweet': retweeted}"></i>
    <i @click="like" class="far fa-heart pointer" :class="{'heart': liked}"></i>
    <i class="fas fa-share pointer"></i>
  </div>
</template>

<script>
export default {
  name: "Actions",
  data(){
    return{
      liked: false,
      retweeted: false,
    }
  },
  methods:{
    like(){
      this.liked = true;
    },
    retweet(){
    this.retweeted = true;
    }
  }
};

</script>

<style>

</style>
