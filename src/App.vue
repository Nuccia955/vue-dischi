<template>
    <div id="app" class="d-flex flex-column h-100">
        <Header />

        <main class="flex-grow-1">
            <CardList />
        </main>
    </div>
</template>

<script>
import Header from '@/components/Header.vue'
import CardList from '@/components/CardList.vue'
export default {
  name: 'App',
  components: {
    Header,
    CardList,
  }
}
</script>

<style lang="scss">
@import '~bootstrap/scss/bootstrap.scss';
@import '@/styles/colors.scss';

body {
  height: 100vh;
  #app {
    background-color: $bg_primary;
    img {
      max-width: 100%;
    }
    ul {
      list-style: none;
      margin: 0;
      padding: 0;
    }
  }
}
</style>
