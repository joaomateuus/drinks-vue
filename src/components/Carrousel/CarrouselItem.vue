<template>
  <transition name="slide-in">
    <div>
      <img :src="banner" v-show="currentSlide === index">
    </div>
  </transition>
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

.slide-in-enter-active,
.slide-in-leave-active{
  transition: all 1s ease-in-out;
}

.slide-in-enter-from {
  transform: translateX(-100%);
}

.slide-in-leave-to{
  transform: translateX(100%);
}
</style>