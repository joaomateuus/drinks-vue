<template>
  <div>
    <div>
      <h1>Hello World</h1>
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
