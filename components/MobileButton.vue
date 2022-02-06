<template>
  <button
    class="mobile-button"
    @click="close"
  />
</template>

<script>
  export default {
    name: 'MobileButton',
     methods: {
      close() {
        this.$emit('close');
      },
    }
  };
</script>

<style lang="scss" scoped>
.mobile-button {
  position: fixed;
  display: flex;
  align-items: center;
  justify-content: center;
  width: 35px;
  height: 35px;
  transition: 0.2s all ease;
  z-index: 10;
  top: 30px;
  right: 5%;
  @include reset-button;
  &::before {
    @include buttonConfig(-10px);
    box-shadow: 0 10px 0 $white;
  }
  &::after {
    @include buttonConfig(10px);
  }
}
.mobile-button.button--active {
  z-index: 11;
  &::before {
    box-shadow: 0 0 0 $white;
    transform: translateY(0px) rotate(45deg);
  }
  &::after {
    transform: translateY(0px) rotate(-45deg);
  }
}
</style>
