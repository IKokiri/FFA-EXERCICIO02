<template>
  <div id="app">
    <ProductList v-bind:products=products />    
    <ProductForm/>
    Total de Produtos: {{totalProducts}}
  </div>
</template>

<script>
import ProductList from './components/ProductList.vue'
import ProductForm from './components/ProductForm.vue'

export default {
  name: 'App',
  data(){
    return {
      products:[
        {
          produto:'p1',
          descricao:'d1',
        },
        {
          produto:'p2',
          descricao:'d2',
        },
        {
          produto:'p2',
          descricao:'d2',
        }
      ]
    }
  },
  computed: {
    totalProducts:function(){
      return this.products.length;
    }
  },
  components: {
    ProductList,
    ProductForm
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

