<template>
  <div class="container">
    <v-card elevation="10" outlined>
      <v-card-title>
        <v-avatar size="30">
          <img src="/img/avataaars1.png" alt="Ada" />
        </v-avatar>
        <h5>AdaDeSions</h5>
      </v-card-title>
      <v-card-text>
        <v-row class="mx-0">
          <p class="content">
            {{ content }}
          </p>
        </v-row>
        <v-row>
          <v-col cols="4">
            <v-btn class="mx-2" fab dark small color="#F2522E">
              <v-icon dark> mdi-heart </v-icon>
            </v-btn>
          </v-col>
          <v-col cols="4">
            <v-btn class="mx-2" fab dark small color="#80BF41">
              <v-icon dark> mdi-baby-face </v-icon>
            </v-btn>
          </v-col>
          <v-col cols="4">
            <v-btn class="mx-2" fab dark small color="#049DD9">
              <v-icon dark> mdi-cloud-download </v-icon>
            </v-btn>
          </v-col>
        </v-row>
      </v-card-text>
    </v-card>
  </div>
</template>

<script>
export default {
  name: "TweetFeed",
  props: ["content", "index"],
};
</script>

<style>
.tweet-feed {
  border: 1px solid greenyellow;
  margin-bottom: 1em;
  color: white;
}

.content {
  font-size: 22px;
  padding-top: 1em;
}
</style>