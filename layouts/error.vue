<template>
  <section class="text-center">
    <p class="error">
      404
    </p>
    <h1 v-if="error.statusCode === 404" class="mb-8">
      Page not found
    </h1>
    <h1 v-else class="mb-8">
      An error occurred
    </h1>

    <nuxt-link to="/" class='px-4 py-2 border border-primary-500 text-primary-500 rounded hover:bg-primary-200 dark:hover:bg-primary-700'>
      Go back to home page
    </nuxt-link>
  </section>
</template>
<script>
  export default {
    props: {
      error: {
        type: Object,
        default: () => {}
      }
    }
  }
</script>
<style scoped>
  .error {
    font-size: 120px;
  }
</style>
