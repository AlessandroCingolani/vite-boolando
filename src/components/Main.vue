<script>
import ProductCard from './partials/ProductCard.vue';
export default {
  name:'Main',
  components:{
    ProductCard
  }
}
</script>

<template>
  <main>
    <div class="container">
      <div class="product-card d-flex">

       <ProductCard/>

        

        
        

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