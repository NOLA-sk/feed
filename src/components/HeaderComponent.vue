<template>
  <header class="header">
    <div class="container">
      <a href="/" class="logo-link">
        <img class="logo" src="../assets/happy.png" alt="cat-logo"
      /></a>
      <nav class="nav">
        <a class="nav__link" href="/feed">Моя лента</a>
        <a class="nav__link" href="#">По имени пользователя</a>
        <a class="nav__link" href="#">По хэштегу</a>
      </nav>
    </div>
  </header>
</template>

<script>
export default {};
</script>

<style lang="sass" scoped>
.header
    padding: 20px 50px
    border-bottom: 2px solid #8666c3
.container
    width: 100%
    display: flex
    justify-content: space-between
.logo
    max-width: 80px
    max-height: 80px
    transition: all 0.3s
    &:hover
        transform: scale(1.1)
.nav
    display: flex
    justify-content: space-between
    padding: 30px 0
    &__link
        text-decoration: none
        font-size: 20px
        margin-left: 20px
        transition: all 0.3s
        &:hover
            transform: scale(1.1)
            text-shadow: 1px 1px 2px #8666c3
</style>
