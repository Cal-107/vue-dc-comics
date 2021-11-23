<template>
  <section class="content-container">
      <div class="container">
        --> Content goes here
      </div>
  </section>
</template>

<script>
export default {
    name: 'Content',
}
</script>

<style lang="scss" scoped>

    .content-container {
        display: flex;
        flex-direction: column;
        justify-content: center;
        color: #fff;
        background-color: #1c1c1c;
        height: 100%;
        .container {
            width: 100%;
        }
    }

</style>