<template>
    <div id="Product-List-One">
        <h2>Product List One</h2>
        <ul>
            <li v-for="(product,index) in saleProducts" :key="index">
                <span class="name">{{ product.name }}</span>
                <span class="price">{{ product.price }}</span>
            </li>
        </ul>   
        <button v-on:click="reducePrice(4)">Reduce Price</button>
    </div>
</template>

<script>    
import {mapGetters} from 'vuex';
import {mapActions} from 'vuex';

export default {
  computed: {
      products(){
          return this.$store.state.products;
      },
      ...mapGetters([
          'saleProducts'
      ])
  }, 
  methods: {
      ...mapActions([
          'reducePrice'
      ])
  }
}
</script>

<style scoped>

</style>
