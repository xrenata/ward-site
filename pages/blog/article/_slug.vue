<template>
    <article class="grid justify-center m-auto text-center">
      <div>
        <header class="m-auto max-w-6/12 space-y-2 text-center">
          <div class="space-y-2">
            <h1 class="text-2xl font-semibold text-gray-200">
              {{ article.title }}
            </h1>

            <p class="text-gray-400 text-center">
              {{ article.description }}
            </p>
          </div>
        </header>
        <div>
          <div class="m-auto flex-col justify-center text-gray-100 max-w-10/12 text-left">
            <nuxt-content :document="article" />
          </div>
        </div>
      </div>
    </article>
</template>

<script>
export default {
  async asyncData({ $content, params }) {
    const article = await $content("article", params.slug).fetch();
    return { article };
  },
};
</script>

<style>
</style>