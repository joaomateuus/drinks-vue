<template>
  <div>
    <div class="carrousel-item">
      <img v-for="slide in slides" :src="slide" />
    </div>
  </div>
</template>

<script>

export default {
  name: 'CarrouselItem',
  components: {},
  data: () => ({
    slides: [
      'https://picsum.photos/id/1002/4312/2868',
      'https://picsum.photos/id/1000/5626/3635',
      'https://picsum.photos/id/1005/5760/3840',
      'https://picsum.photos/id/1012/3973/2639'
    ]
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