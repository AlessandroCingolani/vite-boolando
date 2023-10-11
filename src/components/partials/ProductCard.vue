<script>

export default {
  name:'ProductCard',
  props:{
    productObj: Object
  },

  data (){
    return {

    }
  },

  computed: {
    price(){
      return this.productObj.lastPrice.toFixed(2 ,'0').replace(".", ",");
    }

  }
  
}
</script>

<template>
  <!-- box-img product -->
  <div class="col-product">
    <div class="box-img">
      <a href=""><img :src="`/img/${productObj.primaryImage}`" alt="img1"></a>
      <a href="#"><img class="hidden" :src="`/img/${productObj.secondaryImage}`" alt=""></a>
      <span class="heart">&hearts;</span>
      <div class="labels">
        <span class="discount" v-if="(productObj.discount != null)">{{productObj.discount }}</span>
        <span class="green-piece" v-if="(productObj.sostenibilita)">Sostenibilità</span>
      </div>
    </div>

    <!-- name and price product -->
    <div class="details-product">
      <h6>{{ productObj.marca }}</h6>
      <h4>{{ productObj.modello }}</h4>
      <span class="product-actual-price">{{ `${price} €` }}</span>
      <span class="product-old-price" v-if="(productObj.fullPrice != null)">{{ `${productObj.fullPrice} €` }}</span>
    </div>
  </div>
</template>


<style lang="scss">
@use '../../scss/partials/variables' as *;
  .col-product {
    width: calc(100% / 3);
    padding: 10px;
    position: relative;
    img {
      width: 100%;
    }
    .box-img {
      position: relative;

      &:hover .hidden {
        display: block;
      }

      .heart {
        font-size: 1.5rem;
        background-color: white;
        padding: 5px 10px;
        position: absolute;
        top: 10px;
        right: 0;

        &:hover {
          color: $discount-color;
          cursor: pointer;
        }
      }
      .labels {
        color: white;
        position: absolute;
        bottom: 40px;
        .green-piece {
          padding: 2px 5px;
          background-color: $green-piece;
        }
        .discount {
          background-color: $discount-color;
          padding: 2px 5px;
          margin-right: 3px;
        }
      }
    }
    .details-product {
      h6 {
        color: $brand-color;
        padding-bottom: 1px;
      }
      
      h4 {
        text-transform: uppercase;
      }
      .product-actual-price {
        color: $discount-color;
        font-weight: 800;
        margin-right: 3px;
      }
    
      .product-old-price {
        text-decoration: line-through;
      }
    }
  }
</style>