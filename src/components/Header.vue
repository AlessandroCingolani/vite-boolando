  <script>
  import { gender,icons } from '../data/header-menu';
  export default {
    name:'Header',
    data(){
      return {
        gender,
        icons
      }
    }

  }
  </script>
  
<template>
    
  <header>
    <div class="top-fixed">
      <div class="container header-bar d-flex">

        <div class="gender">
          <a v-for="(type,index) in gender"
          :key="index" :href="type.href">{{type.text}}</a>
        </div>

        <div class="logo">
          <a href="#"><img src="../assets/img/boolean-logo.png" alt="logo"></a>
        </div>
        
        <nav class="top-icons">
          <ul>
            <li v-for="(icon,index) in icons" :key="index">
              <a :href="icon.href"><i :class="icon.icon"></i></a>
            </li>
          </ul>
        </nav>
    
      </div>
    </div>
  </header>

</template>


<style lang="scss" scoped>
@use '../scss/partials/variables' as *;
  header{
    .top-fixed {
      width: 100%;
      position: fixed;
      box-shadow: 0px 0px 15px $brand-color;
      top:0;
      left: 0;
      padding: 12px;
      background-color:$header-background;
      z-index: 999;
    }
  } 

  .container.header-bar {
    justify-content: space-between;
    align-items: center;
  }

  .logo {
    a {
      img {
        width: 120px;
      }
    }
  } 
  .gender {
    a {
      padding-right: 10px;
    }
  } 

</style>
