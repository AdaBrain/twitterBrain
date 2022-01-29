<template>
  <div class="homepage container">
    <div class="row">
      <div class="col-3 col-lg-3 border-right">Left</div>
      <div class="col-6 col-md-6 col-lg-6">
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
                  />
                </div>
              </div>
              <div class="row">
                <div class="col"></div>
                <div class="col-3">
                  <button class="btn btn-sm btn-primary">Tweet</button>
                </div>
              </div>
            </div>
          </div>
          <div class="row">
            <div class="col">
              <p><strong>Preview</strong></p>
              <div class="preview-box border">
                {{ tweet }}
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="col-3 col-lg-3 border-left">Right</div>
    </div>
  </div>
</template>

<script>
export default {
  name: "IndexPage",
  data() {
    return {
      tweet: "",
    }
  }
};
</script>

<style>
body {
  background-color: black;
}

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