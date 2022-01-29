<template>
  <div class="homepage container">
    <div class="row">
      <div class="col-3 col-lg-3 border-right">
        Left
      </div>
      <div class="col-6 col-md-6 col-lg-6">
        <div class="tweet-box container border">
          <div class="row">
            <div class="col-3 border-right">
              <img src="https://previews.123rf.com/images/pandavector/pandavector1704/pandavector170400314/75968328-avatar-of-a-man-in-a-shirt-avatar-and-face-single-icon-in-cartoon-style-vector-symbol-stock-illustra.jpg" class="avatar img-thumbnail mx-auto d-block" alt="">
            </div>
            <div class="col">
              <div class="row">
                <input class="tweet-input" type="text">
              </div>
              <div class="row">
                button
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="col-3 col-lg-3 border-left">
        Right
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'IndexPage'
}
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
</style>