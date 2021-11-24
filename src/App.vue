<template>
  <div id="app">
    <!-- Start Header -->
    <Header />

    <!-- Start Main -->
    <main>
      <Hero />
      <Content />
    </main>

    <!-- Start Footer -->
    <Footer />
  </div>
</template>

<script>
import Header from '@/components/Header.vue';
import Content from '@/components/Content.vue';
import Hero from '@/components/Hero.vue';
import Footer from '@/components/Footer.vue';

export default {
  name: 'App',
  components: {
    Header,
    Hero,
    Content,
    Footer,
  }
}
</script>

<style lang="scss">

  @import '@/styles/utilities';
  @import '@/styles/globals';

</style>
