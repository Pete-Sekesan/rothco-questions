<template>
  <div>
    <form @submit.prevent='createPost'>
      <label for="title">Title</label><br />
      <input type="text" id="title" v-model="formData.title" /> <br/>
      <label for="body">Body</label><br />
      <input type="text" id="body" v-model="formData.body" /> <br/>
      <button>Submit</button>
    </form>
  </div>
</template>

<script>
import axios from "axios";

export default {
  name: "CreatePost",
  data() {
    return {
      formData: {
        title: "",
        body: "",
      },
    };
  },
  methods: {
    createPost() {
      axios
        .post("https://jsonplaceholder.typicode.com/posts", this.formData)
        .then((response) => console.log(response))
        .catch((error) => console.log(error));
    },
  },
};
</script>

<style scoped>
</style>
