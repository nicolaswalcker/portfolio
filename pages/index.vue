<template>
  <main class="main">
    <particles-container />
    <section id="start"></section>
    <section id="skills"></section>
    <section id="works"></section>
    <section id="about"></section>
  </main>
</template>

<script>
import ParticlesContainer from '~/components/ParticlesContainer.vue'
export default {
  name: 'IndexPage',
  components: { ParticlesContainer },
}
</script>
<style lang="scss" scoped>
.main {
  background: $dark-200;
  min-height: 100vh;
  @include breakpoint(small-up) {
    min-height: calc(100vh - 85px);
  }
}
section {
  height: 100%;
}
</style>
