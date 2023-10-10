<script>
export default {
  name:'Footer'
}
</script>

<template>
  <footer>
    <div class="container">
      <div class="foot-box d-flex">

        <div class="information-footer">
          <a href="#"><h4>Booleando s.r.l</h4></a>
          <a href="#"><span>Informazioni legali</span></a>
          <a href="#"><span>Informativa sulla privacy</span></a>
          <a href="#"><span>Diritto di recesso</span></a>
        </div>

        <nav class="footer-icons">
          <h5>Trovaci anche su</h5>
          <ul>
            <li><a href="#"><i class="fa-brands fa-square-twitter"></i></a></li>
            <li><a href="#"><i class="fa-brands fa-square-facebook"></i></a></li>
            <li><a href="#"><i class="fa-brands fa-square-instagram"></i></a></li>
            <li><a href="#"><i class="fa-brands fa-square-pinterest"></i></a></li>
            <li><a href="#"><i class="fa-brands fa-square-youtube"></i></a></li>
          </ul>
        </nav>

        
      </div>
    </div>
  </footer>
</template>


<style lang="scss" scoped>
@use '../scss/partials/variables' as *;
  footer {
    background-color: black;
    color: white;
    .foot-box {
      justify-content: space-between;
      align-items: center;
      padding: 20px;
    }
  }
  .footer-icons {
    h5 {
      text-align: center;
      padding-bottom: 5px;
      font-size: .9rem;
    }
  } 

  .information-footer{
    a {
     span {
       font-size: .8rem;
       padding: 5px 5px 0 0;
     }
    }
  }
</style>