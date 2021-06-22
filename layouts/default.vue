<template>
  <div class="w-min-screen h-min-screen bg-background">
    <NavBarArticle v-if="$route.name.includes('article')" />
    <NavBarBlog v-else-if="$route.name.includes('blog')" />
    <NavBarHeader v-else />
    <Nuxt class="min-h-screen"/>
    <NavBarFooter class="mt-4"/>
  </div>
</template>

<style>
/* width */
::-webkit-scrollbar {
  width: 5px;
  height: 5px;
}

/* Track */
::-webkit-scrollbar-track {
  background: #24252a;
}

/* Handle */
::-webkit-scrollbar-thumb {
  background: #16609b;
}

/* Handle on hover */
::-webkit-scrollbar-thumb:hover {
  background: #4283b8;
}
</style>
