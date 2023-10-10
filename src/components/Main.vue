<script>
export default {
  name:'Main'
}
</script>

<template>
  <main>
    <div class="container">
      <div class="product-card d-flex">

        <!-- box-img product -->
        <div class="col-product">
          <div class="box-img">
            <a href=""><img src="../assets/img/1.webp" alt="img1"></a>
            <a href="#"><img class="hidden" src="../assets/img/1b.webp" alt=""></a>
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

        <div class="col-product">
          <div class="box-img">
            <img src="../assets/img/2.webp" alt="img2">
            <a href="#"><img class="hidden" src="../assets/img/2b.webp" alt=""></a>
            <span class="heart">&hearts;</span>
            <span class="discount">-30%</span>
          </div>

          <div class="details-product">
            <h6>Guess</h6>
            <h4>ROSES TEE</h4>
            <span>20,99€</span>
            <span>29,99€</span>
          </div>
        </div>

        <div class="col-product">
          <div class="box-img">
            <img src="../assets/img/3.webp" alt="im3g">
            <a href="#"><img class="hidden" src="../assets/img/3b.webp" alt=""></a>
            <span class="heart">&hearts;</span>
            <span class="discount">-30%</span>
          </div>

          <div class="details-product">
            <h6>Come Zucchero Filato</h6>
            <h4>VOGLIA DI COLORI PASTELLO</h4>
            <span>129,99€</span>
            <span>184,99€</span>
          </div>
        </div>

        <div class="col-product">
          <div class="box-img">
            <img src="../assets/img/4.webp" alt="img4">
            <a href="#"><img class="hidden" src="../assets/img/4b.webp" alt=""></a>
            <span class="heart">&hearts;</span>
            <span class="discount">-50%</span>
            <span class="green-piece">Sostenibilità</span>
          </div>

          <div class="details-product">
            <h6>Levi's</h6>
            <h4>TEE UNISEX</h4>
            <span>14,99€</span>
            <span>29.99€</span>
          </div>
        </div>

        <div class="col-product">
          <div class="box-img">
            <img src="../assets/img/5.webp" alt="img5">
            <a href="#"><img class="hidden" src="../assets/img/5b.webp" alt=""></a>
            <span class="heart">&hearts;</span>
          </div>

          <div class="details-product">
            <h6>Maya Deluxe</h6>
            <h4>STRIPE BODICE</h4>
            <span>99,99€</span>
          </div>
        </div>

        <div class="col-product">
          <div class="box-img">
            <img src="../assets/img/6.webp" alt="img6">
            <a href="#"><img class="hidden" src="../assets/img/6b.webp" alt=""></a>
            <span class="heart">&hearts;</span>
            <span class="green-piece alone">Sostenibilità</span>
          </div>

          <div class="details-product">
            <h6>Esprit</h6>
            <h4>MAGLIONE - BLACK</h4>
            <span>29,99€</span>
          </div>
        </div>

      </div>
    </div>
  </main>
</template>


<style lang="scss" scoped>
@use '../scss/partials/variables' as *;
  .container {
    .product-card {
     justify-content: center;
     flex-wrap: wrap;
     width: 100%;
     margin-top: 100px;
     padding-bottom: 30px;
   }
  }

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