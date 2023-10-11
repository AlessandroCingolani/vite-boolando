<script>
import ProductCard from './partials/ProductCard.vue';
import products from '../data/products';
export default {
  name:'Main',
  components:{
    ProductCard
  },
  data(){
    return {
      products
    }
  }
}
</script>

<template>
  <main>
    <div class="container">

      <div class="product-card d-flex">

       <ProductCard v-for="product in products" :key ="product.id" :productObj="product"/>

      </div>

    </div>
  </main>
</template>


<style lang="scss" scoped>
@use '../scss/partials/variables' as *;
  .product-card {
      justify-content: center;
      flex-wrap: wrap;
      width: 100%;
      margin-top: 100px;
      padding-bottom: 30px;
    }

</style>