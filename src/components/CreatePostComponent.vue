<template>
  <form class="form" @submit.prevent>
    <input
      class="input"
      type="text"
      placeholder="Мой новый пост"
      v-model="post.text"
    />
    <button class="btn" type="submit" @click="createPost">Создать</button>
  </form>
</template>

<script>
export default {
  data() {
    return {
      post: {
        text: "",
        author: "Me",
      },
    };
  },
  methods: {
    createPost() {
      console.log("click->post");
      this.post.id = Date.now();
      this.$emit("getNewPost", this.post);
      this.post = {
        text: "",
        author: "Me",
      };
    },
  },
};
</script>

<style lang="sass" scoped>
.form
  display: flex
  flex-direction: column
.input
  border: 2px solid #8666c3
  border-radius: 5px
  padding: 5px
  transition: all 0.3s
  min-height: 50px
  width: 100%
  font-size: 18px
  &:focus
    background: #fff
    outline: none

.btn
  width: 150px
  height: 50px
  border: 2px solid #8666c3
  border-radius: 5px
  transition: all 0.3s
  font-size: 18px
  margin-top: 15px
  &:hover
    transform: scale(1.01)
    box-shadow: 3px 3px 2px 2px #8666c3
    background: #c7c7ef
</style>
