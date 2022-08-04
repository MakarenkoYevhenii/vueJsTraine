<template>
  <div class="hello">
    <PostForm  @create="createPost"  />
    <PostList :posts="posts"/>
  </div>
</template>

<script>
import PostForm from '@/components/postForm'
import PostList from '@/components/postList';
export default {

  data() {
    return {
      posts: [
        { id: 1, tittle: "javascript", body: "tut chto-to o javascripte" },
        { id: 2, tittle: "javascript1", body: "tut chto-to o javascripte1" },
      ],
    };
  },
  name: "HelloWorld",
  props: {
    msg: String,
  },
  methods:{
    createPost(post){
      this.posts.push(post)
    }
  },
  components: { PostForm, PostList }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
</style>
