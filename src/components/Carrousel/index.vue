<template>
  <div>
    <div class="carrousel">
      <div class="carrousel-inner">
        <CarrouselItem v-for="(banner, index) in banners" :key="`item-${index}`" :banner="banner" :current-slide="currentSlide" :index="index"  />
      </div>
    </div>
  </div>
</template>

<script>
import CarrouselItem from "@/components/Carrousel/CarrouselItem";

export default {
  name: 'Home',
  components: {
    CarrouselItem
  },
  data: () => ({
    currentSlide: 0,
    slideInterval: null,
    banners: [
      'https://picsum.photos/id/1002/4312/2868',
      'https://picsum.photos/id/1000/5626/3635',
      'https://picsum.photos/id/1005/5760/3840',
      'https://picsum.photos/id/1012/3973/2639'
    ]
  }),
  methods: {
    setCurrentSlide(index){
      this.currentSlide = index;
    }
  },
  mounted() {
    this.slideInterval = setInterval(()=> {
      const index = this.currentSlide < this.banners.length -1 ? this.currentSlide +1 : 0
      this.setCurrentSlide(index);
    }, 3000)
  },
  beforeMount() {
    clearInterval(this.slideInterval)
  }
}
</script>
<style>
.carrousel{
  display: flex;
  justify-content: center;
}

.carrousel-inner {
  position: relative;
  width: 900px;
  height: 400px;
  overflow: hidden;
}
</style>
