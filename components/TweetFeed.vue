<template>
  <div class="tweet-feed container">
      {{ content }}
  </div>
</template>

<script>
export default {
    name: "TweetFeed",
    props: ["content"],
}
</script>

<style>
.tweet-feed {
    border: 1px solid greenyellow;
    margin-bottom: 1em;
    color: white;
}

</style>