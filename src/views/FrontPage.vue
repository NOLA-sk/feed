<template>
  <header-component />
  <div class="description">
    <h1 class="description__title">
      Привет, ты сейчас смотришь на мое тестовое приложение!
    </h1>
    <p class="description__text">
      Это приложение было написано для того, чтобы понять как работает Vue.
      Функционал здесь довольно прост, но для тренировки навыков, думаю самое
      то. Надеюсь, что у меня хоть что-то из этого получилось
    </p>
  </div>
</template>

<script>
import HeaderComponent from "@/components/HeaderComponent.vue";
export default {
  components: {
    HeaderComponent,
  },
  data() {
    return {};
  },
};
</script>
<style lang="sass" scoped>
.description
    text-align: center
    &__title
        margin: 30px 0
    &__text
        font-size: 20px
        max-width: 1000px
        margin: auto
</style>
