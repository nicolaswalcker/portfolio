<template>
  <nav class="navigation">
    <ul class="navigation__content">
      <li class="navigation__item">
        <a class="navigation__link" href="#start"> Início </a>
      </li>
      <li class="navigation__item">
        <a class="navigation__link" href="#skills"> Conhecimentos </a>
      </li>
      <li class="navigation__item">
        <a class="navigation__link" href="#works"> Trabalhos </a>
      </li>
      <li class="navigation__item">
        <a class="navigation__link" href="#about"> Sobre mim </a>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: 'NavBar',
}
</script>

<style lang="scss" scoped>
.navigation {
  position: sticky;
  width: 100%;
  height: 5.3125rem;
  top: 0;
  z-index: 10;
  border-bottom: $border-1 solid rgba(255, 255, 255, 0.1);
  background: $dark-200;
  &__content {
    display: flex;
    align-items: center;
    justify-content: space-around;
    height: auto;
    padding: 1.5rem 0;
  }

  &__link {
    font-size: $text-3xl;
    position: relative;

    @include hover-effect;
  }
}
</style>
