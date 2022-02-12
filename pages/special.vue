<template>
  <div class="special container">
    <div class="row">
      <div class="col-12">
        <button id="submit" class="my-btn" @click="onClickSubmit">
          Submit
        </button>
        <button id="delete" class="my-btn" @click="onClickDelete">
          Delete
        </button>
        <button id="info" class="my-btn" @click="onClickInfo">Info</button>
      </div>
    </div>

    <!-- Result Zone -->
    <div class="row result-container">
      <div class="col-12">
        <p :class="[resultClass, 'ada']">
          {{ result }}
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data: () => {
    return {
      result: "Your result will show here.",
      resultClass: ""
    };
  },

  methods: {
    onClickSubmit() {
      this.result = "You clicked on submit button";
      this.resultClass = "submit-result"
    },
    onClickDelete() {
      this.result = "The element was deleted!";
      this.resultClass = "delete-result"
    },
    onClickInfo() {
      this.result = "This is your information.";
      this.resultClass = ""
    },
  },
};
</script>


<style>
/* CSS Zone */
body {
  background-color: #f2cf66;
}

.my-btn {
  /* margin-left: 1em; */
  margin-top: 1em;
  height: 3em;
  width: 8em;
  font-weight: bold;
  border: none;
  color: #fff;
}

#submit {
  background-color: rgba(54, 217, 111, 1);
}

#submit:hover {
  color: rgba(54, 217, 111, 0.7);
  border: 2px solid rgba(54, 217, 111, 1);
  background-color: rgba(0, 0, 0, 0);
}

#delete {
  background-color: rgba(242, 84, 48, 1);
}

#delete:hover {
  color: rgba(242, 84, 48, 0.7);
  border: 2px solid rgba(242, 84, 48, 1);
  background-color: rgba(0, 0, 0, 0);
}

#info {
  background-color: rgba(73, 211, 242, 1);
}

#info:hover {
  color: rgba(73, 211, 242, 1);
  border: 2px solid rgba(73, 211, 242, 1);
  background-color: rgba(0, 0, 0, 0);
}

.result-container {
  border: 3px solid #fff;
  height: 5em;
  margin-top: 1em;
}

.submit-result {
    font-weight: bold;
    color: rgba(54, 217, 111, 1)
}

.delete-result {
    font-weight: bold;
    color: rgba(255, 0, 0, 1) 
}
</style>