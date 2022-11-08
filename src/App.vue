<template>
  <h2>Name : {{ nama }}</h2>
  <button @click="changeName">Change Name</button>
</template>

<script>


export default {
  name: 'App',
  data() {
    return {
      nama: "Muhammad Afiv"
    };
  },
  methods: {
    changeName() {
      this.nama = "Afiv";
    }
  }
}
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
