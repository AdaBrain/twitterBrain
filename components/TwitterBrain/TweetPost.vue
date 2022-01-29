<template>
  <div class="tweet-post container">
    <div class="row">
      <div class="col-3">
        <img
          :src="avatar"
          alt=""
          class="avatar img-thumbnail d-block"
        />
      </div>
      <div class="col">
          <p class="tweet-content"> {{tweet}} </p>
          <p class="datetime"> {{datetime}} </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "TweetPost",
  props: {
    avatar: String,
    tweet: String,
    datetime: String,
  },
};
</script>

<style>
.tweet-post {
    color: white;
    margin-top: 1em;
    border: 1px solid rgba(128, 128, 128, 0.5);
    border-radius: 1em;
}

.avatar {
  border-radius: 100%;
  width: 3em;
  height: auto;
}
</style>