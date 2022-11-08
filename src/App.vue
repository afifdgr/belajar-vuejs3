<template>
  <div v-if="products.length">
    <ul>
      <li v-for="product in products" :key="product.id">
        {{ product.title }} - {{ product.price }}
      </li>
    </ul>
  </div>
  <div v-else>
    <p>Data Not Found</p>
  </div>
</template>

<script>


export default {
  name: 'App',
  data() {
    return {
      products: []
    };
  },
  created() {
    this.products = [
      { id: 1, title: "Product 1", price: 3000 },
      { id: 2, title: "Product 2", price: 5000 },
      { id: 3, title: "Product 3", price: 7000 },
      { id: 4, title: "Product 4", price: 1000 }
    ];
  },
  /* beforeCreate() {
    console.log('Before Create')
  },
  beforeMount() {
    console.log('Before Mount')
  },
  mounted() {
    console.log('Mounted')
  } */
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
