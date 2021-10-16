<template>
  <div>
    <form @submit='postInput' method='post'>
      <label for= 'title'>Title</label><br>
      <input type='text' name= 'title' > <br><br>
      <label for= 'body'>Body</label><br>
      <input type='text' name= 'body'> <br><br>
      <button type='submit'>Submit</button>

    </form>
  </div>
</template>

<script>
export default {
  name: 'PostForm',
  data () {

  },
  methods:{
    postInput()
    {

    }
  }
};
</script>
