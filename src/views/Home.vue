<template>
  <div class="home">
    <header>
      <Navbar />
    </header>
    <div>
      <Carrousel />
    </div>
    <div>
      <DrinksList />
    </div>
  </div>
</template>

<script>
import Navbar from '../components/Header/Navbar'
import DrinksList from "@/components/DrinksList";
import Carrousel from '../components/Carrousel/index'

export default {
  name: 'Home',
  components: {
    DrinksList,
    Carrousel,
    Navbar
  }
}
</script>
