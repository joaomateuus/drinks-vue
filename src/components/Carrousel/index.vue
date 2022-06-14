<template>
  <div>
    <div class="carrousel">
      <div class="carrousel-inner">
        <CarrouselItem />
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

  }),
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
