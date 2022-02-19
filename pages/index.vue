<template>
  <div class="homepage container">
    <div class="row">
      <div class="col-3 col-lg-3 border-right">Left</div>
      <div class="col-6 col-md-6 col-lg-6">
        <tweet-post></tweet-post>
      </div>
      <div class="col-3 col-lg-3 border-left">
        <v-card
          class="mx-auto"
          color="#26c6da"
          dark
          max-width="400"
          loading="#FF0000"
        >
          <v-card-title>
            <v-icon large left> mdi-antenna </v-icon>
            <span class="text-h6 font-weight-light"> News </span>
          </v-card-title>

          <v-card-text class="my-text text-h5 font-weight-bold">
            {{ cardText }}
          </v-card-text>

          <v-card-actions>
            <v-list-item class="grow">
              <v-list-item-avatar color="grey darken-3">
                <v-avatar size="100">
                  <img
                    src="/img/avataaars1.png"
                    alt="Ada"
                  />
                </v-avatar>
              </v-list-item-avatar>

              <v-list-item-content>
                <v-list-item-title>
                  {{ user }}
                </v-list-item-title>
              </v-list-item-content>

              <v-row align="center" justify="end">
                <v-icon class="mr-1" small> mdi-heart </v-icon>
                <span class="subheading mr-2">
                  {{ loveNum }}
                </span>
                <span class="mr-1">·</span>
                <v-icon class="mr-1" small> mdi-share-variant </v-icon>
                <span class="subheading">
                  {{ sharedNum }}
                </span>
              </v-row>
            </v-list-item>
          </v-card-actions>
        </v-card>
      </div>
    </div>
  </div>
</template>

<script>
import TweetPost from "../components/TweetPost.vue";

export default {
  name: "IndexPage",
  components: {
    TweetPost,
  },
  data: () => {
    return {
      cardText: "Hello, Ada!",
      user: "AdaBrain",
      loveNum: 1200,
      sharedNum: "16K",
    };
  },
};
</script>

<style>
body {
  background-color: black;
}

.my-text {
  font-size: 20px;
  font-weight: bold;
  line-height: 1.5em;
}
</style>