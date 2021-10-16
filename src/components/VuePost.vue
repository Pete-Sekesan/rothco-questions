<template>
  <div>
    <form @submit='postInput' method='post'>
      <label for= 'title'>Title</label><br>
      <input type='text' name= 'title' v-model='posts.title' > <br><br>
      <label for= 'body'>Body</label><br>
      <input type='text' name= 'body' v-model='posts.body'> <br><br>
      <button type='submit'>Submit</button>

    </form>
  </div>
</template>

<script>
export default {
  name: 'PostForm',
  data() {
    return {
    posts:{
      title:null,
      body: null
    }
    }
  },
  methods:{
    postInput(e)
    {
      console.warn(this.posts)
      e.preventDefault();
    }
  }
};
</script>
