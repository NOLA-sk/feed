<template>
  <div class="post" :post="post">
    <p class="post__text">
      {{ post.text }}
    </p>
    <p class="post__attributes">Автор: {{ post.author }}</p>
  </div>
</template>
<script>
export default {
  data() {
    return {};
  },
  methods: {},
  props: {
    post: {
      type: Object,
      required: true,
    },
  },
};
</script>
<style lang="sass" scoped>
.post
  margin-top: 30px
  border: 2px solid #8666c3
  border-radius: 5px
  padding: 5px
  transition: all 0.3s
  &:hover
    transform: scale(1.01)
    box-shadow: 3px 3px 2px 2px #8666c3
  &__text
    font-size: 18px
    margin-bottom: 5px
  &__attributes
    font-size: 15px
    font-weight: 700
</style>
