<template>
  <div class="tweet-feed container">
      {{index + 1}} -- {{ content }}
  </div>
</template>

<script>
export default {
    name: "TweetFeed",
    props: ["content", "index"],
}
</script>

<style>
.tweet-feed {
    border: 1px solid greenyellow;
    margin-bottom: 1em;
    color: white;
}

</style>