<template>
    <div id="app">
        <Header />
    </div>
</template>

<script>
import Header from '@/components/Header.vue'
export default {
  name: 'App',
  components: {
    Header,
  }
}
</script>

<style lang="scss">
@import '~bootstrap/scss/bootstrap.scss';
@import '@/styles/colors.scss';

body {
  background-color: $bg_primary;
  height: 100vh;
}
</style>
