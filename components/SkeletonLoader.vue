<template>
  <div
    v-if="type === 'image' && imageUrl"
    :style="{
      backgroundImage: itemLoaded === true ? `url('${imageUrl}')` : '',
      backgroundPosition: 'center',
      backgroundSize: itemLoaded === true ? backgroundSize : '',
    }"
  >
    <img
      :src="imageUrl"
      class="invisible"
      draggable="false"
      alt="image"
      width="100%"
      height="100%"
      @load="itemLoaded = true"
    />
  </div>

</template>

<script>
export default {
  props: {
    type: {
      type: String,
      required: false,
      default: "block",
    },
    imageUrl: {
      type: String,
      required: false,
      default: null,
    },
    backgroundSize: {
      type: String,
      required: false,
      default: "cover",
    },
  },
  data() {
    return {
      itemLoaded: false,
    }
  },
}
</script>
