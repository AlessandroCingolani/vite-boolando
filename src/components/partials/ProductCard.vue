<script>

export default {
  name:'PorductCard',
  
}
</script>

<template>
  <!-- box-img product -->
  <div class="col-product">
          <div class="box-img">
            <a href=""><img src="/img/1.webp" alt="img1"></a>
            <a href="#"><img class="hidden" src="/img/1b.webp" alt=""></a>
            <span class="heart">&hearts;</span>
            <span class="discount">-50%</span>
            <span class="green-piece">Sostenibilità</span>
          </div>

          <!-- name and price product -->
          <div class="details-product">
            <h6>Levi's</h6>
            <h4>RELAX FIT TEE UNISEX</h4>
            <span>14,99€</span>
            <span>29,99€</span>
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
    }
  }

  .details-product {
    h4 {
      text-transform: uppercase;
    }
  }

  .details-product :nth-child(3) {
    color: red;
    font-weight: 800;
    margin-right: 3px;
  }

  .details-product :nth-child(4) {
    text-decoration: line-through;
  }


  .box-img:hover .hidden {
    display: block;
  }

  .discount ,.green-piece {
  color: white;
  position: absolute;
  bottom: 60px;
  padding: 1px 5px;
  }

  .discount {
    background-color: $discount-color;
    left: 0;
  }

  .green-piece {
    background-color: $green-piece;
    left: 50px;
  }

  .green-piece.alone {
    left: 0;
  }


  h6 {
    color: $brand-color;
  }
</style>