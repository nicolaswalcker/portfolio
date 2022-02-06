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
}
</style>
