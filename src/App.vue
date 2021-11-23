<template>
  <div id="app" class="container">
    <!-- Start Header -->
    <Header />

    <!-- Start Main -->
    <main></main>

    <!-- Start Footer -->
    <footer></footer>
  </div>
</template>

<script>
import Header from '@/components/Header.vue';

export default {
  name: 'App',
  components: {
    Header,
  }
}
</script>

<style lang="scss">

  @import '@/styles/utilities';
  @import '@/styles/globals';

</style>
