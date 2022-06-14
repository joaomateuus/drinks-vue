<template>
  <div class="home">
    <div class="flex flex-row justify-between items-center bg-black h-32">
      <img class="h-12 w-22 ml-4" src="https://www.pngkey.com/png/full/429-4296716_drink-menu-derbys-bar-logo-white-drink-menu.png">
      <div>
        <ul class="flex flex-row justify-evenly w-96 text-white">
          <li>Sobre</li>
          <li>Bebidas</li>
        </ul>
      </div>
    </div>
    <div>
      <DrinksList />
    </div>
  </div>
</template>

<script>
import DrinksList from "@/components/DrinksList";

export default {
  name: 'Home',
  components: {
    DrinksList
  }
}
</script>
