<template>
  <div>
    <img :src="banner" v-show="currentSlide === index">
  </div>
</template>

<script>

export default {
  name: 'CarrouselItem',
  components: {},
  props: ["banner", "currentSlide", "index"],
  data: () => ({

  }),
}
</script>
<style>
.carrousel-item{
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
}
</style>