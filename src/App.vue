<template>
  <div id="app">
    <Product-List-One></Product-List-One>
    <Product-List-Two></Product-List-Two>
  </div>
</template>

<script>
import ProductListOne from './components/ProductListOne.vue';
import ProductListTwo from './components/ProductListTwo.vue';

export default {
  name: 'App',
  components: {
    'Product-List-One': ProductListOne,
    'Product-List-Two': ProductListTwo,
  },
  data() {
    return {
      
    }
  }
}
</script>

<style>
</style>
