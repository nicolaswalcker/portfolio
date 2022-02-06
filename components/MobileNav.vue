<template>
  <nav class="navigation">
    <ul class="navigation__content">
      <li class="navigation__item" @click="timeToClose">
        <a class="navigation__link" href="#"> Início </a>
      </li>
      <li class="navigation__item" @click="timeToClose">
        <a class="navigation__link" href="#skills"> Conhecimentos </a>
      </li>
      <li class="navigation__item" @click="timeToClose">
        <a class="navigation__link" href="#works"> Trabalhos </a>
      </li>
      <li class="navigation__item" @click="timeToClose">
        <a class="navigation__link" href="#about"> Sobre mim </a>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: 'MobileNav',
  components: {},
  methods: {
    closeNavBar() {
      this.$emit('close')
    },
    timeToClose() {
      setTimeout(() => {
        this.$emit('close')
      }, 500)
    },
  },
}
</script>

<style lang="scss" scoped>
.navigation {
  width: 100%;
  display: block;
  height: 100vh;
  background-color: $dark-200;
  position: fixed;
  top: 0;
  left: 0;
  transition: all 0.5s ease;
  z-index: 10;

  &__content {
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    align-items: flex-start;
    height: 100%;
    padding: 0;
    gap: 3rem;
    padding: 3rem 0 0 3rem;
  }

  &__link {
    font-size: $text-3xl;
    position: relative;
    z-index: 1;

    @include hover-effect;
  }
}
</style>
