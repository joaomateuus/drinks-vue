<template>
  <div class="mb-4">
    <h1 class="mt-2 text-2xl">Lista de Bebidas</h1>
    <div class="flex items-center justify-evenly mt-2">
      <div class="flex flex-col items-center justify-center" v-for="drink in drinks" key="drink.id">
        <div class="flex flex-col items-center justify-center h-fit w-72 border-2 border-black p-4">
          <div>
            <img class="h-38 w-48" src="https://s2.glbimg.com/W2QRvvfeLt57STPhptJ7xdxO_yc=/smart/e.glbimg.com/og/ed/f/original/2020/12/21/receita-drinks-ceia-natal_10.jpg">
          </div>
          <h1 class="text-3xl text-black">{{ drink.name }}</h1>
          <h1 class="text-2xl font-bold text-green-700">R$ 12,00</h1>
          <p class="text-xl text-black">{{ drink.description }}</p>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import axios from 'axios'

export default {
  name: 'DrinksList',
  components: {},
  data: () => ({
    drinks: [],

  }),
  async beforeMount(){
    try {
      await axios.get('http://localhost:8000/drinks/').then((response) => {
        this.drinks = response.data;
        console.log(this.drinks);
      })
    } catch (error){
      console.log(error)
    }
  },
  methods:{}

}

</script>

<style></style>
