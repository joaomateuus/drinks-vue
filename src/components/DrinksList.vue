<template>
  <div class="flex-col items-center justify-center mt-2">
    <div class="flex flex-row items-center justify-evenly">
      <div class="flex-col items-center justify-center h-fit w-72 border-2 border-black p-4">
        <div>
          <img class="h-38 w-48 ml-8" src="https://s2.glbimg.com/W2QRvvfeLt57STPhptJ7xdxO_yc=/smart/e.glbimg.com/og/ed/f/original/2020/12/21/receita-drinks-ceia-natal_10.jpg">
        </div>
        <h1>Drink</h1>
        <h2>R$</h2>
      </div>
      <div class="flex-col items-center justify-center h-fit w-72 border-2 border-black p-4">
        <div>
          <img class="h-38 w-48 ml-8" src="https://s2.glbimg.com/W2QRvvfeLt57STPhptJ7xdxO_yc=/smart/e.glbimg.com/og/ed/f/original/2020/12/21/receita-drinks-ceia-natal_10.jpg">
        </div>
        <h1>Drink</h1>
        <h2>R$</h2>
      </div>
      <div class="flex-col items-center justify-center h-fit w-72 border-2 border-black p-4">
        <div>
          <img class="h-38 w-48 ml-8" src="https://s2.glbimg.com/W2QRvvfeLt57STPhptJ7xdxO_yc=/smart/e.glbimg.com/og/ed/f/original/2020/12/21/receita-drinks-ceia-natal_10.jpg">
        </div>
        <h1>Drink</h1>
        <h2>R$</h2>
      </div>
      <div class="flex-col items-center justify-center h-fit w-72 border-2 border-black p-4">
        <div>
          <img class="h-38 w-48 ml-8" src="https://s2.glbimg.com/W2QRvvfeLt57STPhptJ7xdxO_yc=/smart/e.glbimg.com/og/ed/f/original/2020/12/21/receita-drinks-ceia-natal_10.jpg">
        </div>
        <h1>Drink</h1>
        <h2>R$</h2>
      </div>
    </div>
    <div class="flex flex-row items-center justify-evenly mt-4">
      <div class="flex-col items-center justify-center h-fit w-72 border-2 border-black p-4">
        <div>
          <img class="h-38 w-48 ml-8" src="https://s2.glbimg.com/W2QRvvfeLt57STPhptJ7xdxO_yc=/smart/e.glbimg.com/og/ed/f/original/2020/12/21/receita-drinks-ceia-natal_10.jpg">
        </div>
        <h1>Drink</h1>
        <h2>R$</h2>
      </div>
      <div class="flex-col items-center justify-center h-fit w-72 border-2 border-black p-4">
        <div>
          <img class="h-38 w-48 ml-8" src="https://s2.glbimg.com/W2QRvvfeLt57STPhptJ7xdxO_yc=/smart/e.glbimg.com/og/ed/f/original/2020/12/21/receita-drinks-ceia-natal_10.jpg">
        </div>
        <h1>Drink</h1>
        <h2>R$</h2>
      </div>
      <div class="flex-col items-center justify-center h-fit w-72 border-2 border-black p-4">
        <div>
          <img class="h-38 w-48 ml-8" src="https://s2.glbimg.com/W2QRvvfeLt57STPhptJ7xdxO_yc=/smart/e.glbimg.com/og/ed/f/original/2020/12/21/receita-drinks-ceia-natal_10.jpg">
        </div>
        <h1>Drink</h1>
        <h2>R$</h2>
      </div>
      <div class="flex-col items-center justify-center h-fit w-72 border-2 border-black p-4">
        <div>
          <img class="h-38 w-48 ml-8" src="https://s2.glbimg.com/W2QRvvfeLt57STPhptJ7xdxO_yc=/smart/e.glbimg.com/og/ed/f/original/2020/12/21/receita-drinks-ceia-natal_10.jpg">
        </div>
        <h1>Drink</h1>
        <h2>R$</h2>
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
