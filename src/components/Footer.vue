<script>
import { info,social } from '../data/footer-menu';
export default {
  name:'Footer',
  data(){
      return {
        info,
        social
      }
    }
}
</script>

<template>
  <footer>
    <div class="container">
      <div class="foot-box d-flex">

        <div class="information-footer">
          <a href="#"><h4>Booleando s.r.l</h4></a>
          <a v-for="(text,index) in info " :key="index" :href="text.href"><span>{{text.text}}</span></a>
        </div>

        <nav class="footer-icons">
          <h5>Trovaci anche su</h5>
          <ul>
            <li v-for="(icon,index) in social " :key="index"><a :href="icon.href"><i :class="icon.icon"></i></a></li>
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