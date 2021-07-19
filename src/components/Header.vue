<template>
  <header class="container pt-3">
      <span class="link">
          <span class="m-3"><a href="#">Download App <span class="ios mt-3 ms-2 p-1 rounded text-white">ios</span> </a></span>
          <span class="m-3"><a href="#">Advertise with us</a></span>
      </span>
      <span class="social float-end">
          <a href="#"><i class="fab fa-facebook-f me-3"></i></a>
          <a href="#"><i class="fab fa-instagram me-3"></i></a>
          <a href="#"><i class="fab fa-twitter me-3"></i></a>
          <a href="#"><i class="fab fa-youtube me-3"></i></a>
      </span>
      <div class="logo m-3 text-center">
          <a href="#"><img :src="require('../assets/avada-food-logo.png')" alt="logo avada food"></a>
      </div>
      <div class="nav mt-4">
          <ul>
              <li class="d-inline-block me-5" v-for="(item,index) in nav" :key="index"><a href="item.url">{{item.text}}</a></li>
              <li class="d-inline-block me-5"><a href="#"><i class="fas fa-search"></i></a></li>
          </ul>
      </div>
  </header>
</template>

<script>
import nav from '@/data/Arraynav.js';
export default {
    name: 'Header',
    data(){
        return{
            nav: nav
        }
    }
}
</script>

<style lang="scss" scoped>
header{
    height: 250px;
 .link{
    .ios{
        background-color: #FC7523;
    }
    a{
        text-decoration: none;
        font-size: 13px;
        color: #525151d7;

        &:hover{
            color: #FC7523;
        }
    }
 }
 .social{
     a{
        color: #9C9894;
     }
 }
 .nav{
    ul{
        list-style: none;
        margin: 0 auto;
        li{
            &:hover{
                border-bottom: 2px solid #FC7523;
            }
            a{
                text-decoration: none;
                color: black;
            }
        }
    }
 }
}
</style>