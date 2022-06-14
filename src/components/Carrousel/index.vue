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
      'https://us.budweiser.com/img/home/desktop/Bud-Supreme-carousel-image.png',
      'https://www.kentucky.com/latest-news/ebvv0c/picture235391842/alternates/FREE_1140/Black%20Lager_Copper%20Lager_glass_bottle.jpg',
      'https://thumbs.dreamstime.com/b/wheat-beer-banner-ads-flying-hops-liquid-d-illustration-golden-tone-background-mountain-141918587.jpg',
      'https://img.freepik.com/free-vector/wheat-beer-banner-blackboard-with-engraved-hops-barrel-3d-style-glass-bottle_317810-1690.jpg?w=2000'
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
