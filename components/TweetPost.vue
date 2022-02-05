<template>
  <div class="tweet-box container">
    <div class="row">
      <div class="col-3">
        <img
          src="https://previews.123rf.com/images/pandavector/pandavector1704/pandavector170400314/75968328-avatar-of-a-man-in-a-shirt-avatar-and-face-single-icon-in-cartoon-style-vector-symbol-stock-illustra.jpg"
          class="avatar img-thumbnail mx-auto d-block"
          alt=""
        />
      </div>
      <div class="col">
        <div class="row">
          <div class="col-12">
            <input
              class="tweet-input"
              type="text"
              placeholder="What's happening?"
              v-model="tweet"
              @keyup.enter="onClickTweet"
            />
          </div>
        </div>
        <div class="row">
          <div class="col"></div>
          <div class="col-3">
            <button @click="onClickTweet" class="btn btn-sm btn-primary">
              Tweet
            </button>
          </div>
        </div>
      </div>
    </div>
    <div class="row">
      <div class="col">
        <p><strong>Preview</strong></p>
        <div v-for="(tw, idx) in tweeted" :key="idx">
          <tweet-feed :content="tw"></tweet-feed>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import TweetFeed from "./TweetFeed.vue";
export default {
  components: { TweetFeed },
  name: "TweetPost",
  data() {
    return {
      tweet: "",
      tweeted: [],
    };
  },
  methods: {
    onClickTweet() {
      this.tweeted.push(this.tweet);
      this.tweet = "";

      console.log(this.tweeted);
    },
  },
};
</script>

<style>
.avatar {
  border-radius: 100%;
  width: 3em;
  height: auto;
}

.tweet-box {
  margin-top: 1em;
}

.tweet-input {
  width: 100%;
  background-color: black;
  color: white;
  border: none;
  margin-bottom: 1em;
}

.tweet-input:focus {
  outline: none;
}

.preview-box {
  color: white;
  font-style: italic;
}
</style>