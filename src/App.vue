<template>
  <input type="text" v-model="cari" placeholder="Cari">

  <ul>
    <li v-for="product in cariData" :key="product.id">
      {{ product.title }} - {{ product.price }}
    </li>
  </ul>

</template>

<script>


export default {
  name: 'App',
  data() {
    return {
      cari: "",
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
  computed: {
    cariData() {
      return this.products.filter((product) => {
        return product.title.match(this.cari);
      });
    }
  }
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
