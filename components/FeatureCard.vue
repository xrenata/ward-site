<template>
  <div class="w-max-24 h-max-24">
    <h2>
      {{ title }}
    </h2>
    <p>
        {{ paragraph }}
    </p>
    <Icon
     :name="icon"
    >
    </Icon>
  </div>
</template>

<script>
export default {
  props: {
    icon: {
      type: String,
      required: true,
    },
    title: {
      type: String,
      required: true,
    },
    paragraph: {
      type: String,
      required: true,
    },
  },
};
</script>

<style>
</style>