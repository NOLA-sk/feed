<template>
  <header-component />

  <div class="container">
    <create-post-component @getNewPost="createNewPost" />
    <post-component :post="post" v-for="post in posts" :key="post.id" />
  </div>
</template>
<script>
import HeaderComponent from "@/components/HeaderComponent.vue";
import PostComponent from "@/components/PostComponent.vue";
import CreatePostComponent from "@/components/CreatePostComponent.vue";
export default {
  components: {
    HeaderComponent,
    PostComponent,
    CreatePostComponent,
  },
  data() {
    return {
      posts: [
        {
          text: "hjhjhhj",
          author: "WSdf",
          id: 1,
        },
        {
          text: "77777j",
          author: "5555",
          id: 2,
        },
        {
          text: "4444",
          author: "WS333df",
          id: 3,
        },
      ],
    };
  },
  methods: {
    createNewPost(newPost) {
      this.posts.push(newPost);
      console.log("we got newPost");
    },
  },
};
</script>
<style lang="sass" scoped>
.container
  margin: 30px
</style>
