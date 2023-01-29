<template>
  <div>
    <form>
      <h2>Add Post</h2>
      <input class="input" type="text" placeholder="Title">
      <input class="input" type="text" placeholder="Description">
      <button>Add</button>
    </form>
    <div class="post" v-for="post in posts">
      <div><strong>Title: </strong>{{post.title}}</div>
      <div><strong>Description: </strong>{{post.body}}</div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      posts: [
        {id: 1, title: 'JS', body: 'DescriptionJS'},
        {id: 1, title: 'Python', body: 'DescriptionPython'},
        {id: 1, title: 'LALLA', body: 'description LALALla'},
      ]
    }
  }
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.app {
  margin: 20px;
}

.post {
  margin: 5px;
  padding: 15px;
  border: 3px solid green;
  background: lawngreen;
  border-radius: 25px;
}

.input {
  width: 300px;
  border: 2px solid green;
  padding: 10px 15px;
  margin-top: 15px;
  border-radius:25px;
}
</style>