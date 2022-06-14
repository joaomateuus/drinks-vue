<template>
  <div>
    <div class="flex flex-row justify-between items-center bg-black h-32">
      <img class="h-12 w-22 ml-4" src="https://www.pngkey.com/png/full/429-4296716_drink-menu-derbys-bar-logo-white-drink-menu.png">
      <div>
        <ul class="flex flex-row justify-evenly w-96 text-white">
          <router-link to="/sobre">
            <li>Sobre</li>
          </router-link>
          <li>Bebidas</li>
        </ul>
      </div>
    </div>
  </div>
</template>
<script>
  export default {
    name: 'Navbar.vue',
    components: {},
    data: () => ({

    }),
  }
</script>
<style>

</style>