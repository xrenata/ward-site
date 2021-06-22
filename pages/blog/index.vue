<template>
  <div class="m-auto justify-center grid text-center">
    <div>
    <h1 class="m-auto text-center"><span class="font-bold text-2xl text-gray-300">Son Gönderiler</span></h1>
    </div>
    <div class="articles grid items-center">
      <div class="my-8 max-w-2xl" v-for="article of articles" :key="article">
        <nuxt-link  :to="article.slug">
          <div class="p-7 bg-gray-600 flex rounded-xl text-gray-100">
            <img
              class="block w-full max-w-screen-sm"
              :src="require(`~/assets/postimg/${article.img}`)"
              alt=""
            />
            <div class="px-4">
              <h3 class="text-gray-200">{{ article.title }}</h3>
              <p>{{ article.description }}</p>
            </div>
          </div>
        </nuxt-link>
      </div>
  </div>
  </div>
</template>

<script>
export default {
  async asyncData({ $content, params }) {
    const articles = await $content("article", params.slug)
      .only(["title", "description", "img", "slug"])
      .sortBy("createdAt", "asc")
      .fetch();
    return {
      articles,
    };
  },
};
</script>

<style>

</style>