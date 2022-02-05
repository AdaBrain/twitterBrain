<template>
  <div class="homepage container">
    <div class="row">
      <div class="col-3 col-lg-3 border-right">Left</div>
      <div class="col-6 col-md-6 col-lg-6">
        <tweet-post></tweet-post>
      </div>
      <div class="col-3 col-lg-3 border-left">Right</div>
    </div>
  </div>
</template>

<script>
import TweetPost from "../components/TweetPost.vue"

export default {
  name: "IndexPage",
  components: {
    TweetPost,
  }
};
</script>

<style>
body {
  background-color: black;
}
</style>