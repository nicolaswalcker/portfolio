<template>
  <header class="header">
    <MobileNav
        v-if="mobileView"
        :style="[{ left: left }]"
        @close="toggleNav"
      />
      <MobileButton
        v-if="mobileView"
        :class="buttonClass"
        @close="toggleNav"
      />
      <NavBar v-if="!mobileView" />
  </header>
</template>

<script>
import MobileNav from '@/components/MobileNav.vue';
import MobileButton from '@/components/MobileButton.vue';
import NavBar from '@/components/NavBar.vue';
  export default {
    name: 'HeaderBar',
    components: {
      NavBar,
      MobileNav,
      MobileButton
    },
    data() {
    return {
      mobileView: false,
      showNav: false,
      buttonClass: '',
      left: '-1000px'
    };
  },
  created() {
    this.verifyWidth();
  },
  mounted() {
    window.addEventListener('resize', this.verifyWidth);
  },
  methods: {
    verifyWidth() {
      this.mobileView = window.innerWidth <= 768;
    },
    toggleNav(){
      this.showNav = !this.showNav;
      this.buttonClass = this.showNav ? 'button--active' : '';
      this.left = this.showNav ? '0' : '-1000px';
    }
  }
  }
</script>
<style lang="scss" scoped>
</style>
