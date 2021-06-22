<template>
  <div>
    <header class="flex flex-col justify-center m-auto text-center">
      <h1 class="text-gray-100 mt-8 m-auto text-center text-5xl">Ward Bot</h1>
      <div class="flex justify-center">
        <SkeletonLoader
          type="image"
          image-url="wardbot-big.png"
          class="w-40 h-40 mt-4 rounded-full ring-4 ring-gray-500"
        />
      </div>
      <p class="mt-4 text-gray-200">Advanced Discord Bot</p>
    </header>
    <section id="features">
      <h1 class="text-gray-100 mt-8 m-auto text-center text-3xl">Features</h1>
      <FeatureCard
        :title="features.title"
        :icon="features.icon"
        :paragraph="features.paragraph"
        class="h-full"
      >
      </FeatureCard>
    </section>
  </div>
</template>

<script>
import FeatureCard from "@/components/FeatureCard.vue"
export default {
  components:{FeatureCard},
  data() {
    return {
      features: [
        {
          title: "Nbr",
          icon: "up",
          paragraph: "asdasdas"
        },
        {

        },
      ],
    };
  },
};
</script>

